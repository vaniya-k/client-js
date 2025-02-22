# Kameleoon JavaScript SDK

## Introduction
Kameleoon JavaScript SDK is used to work with Kameleoon Feature Flags and Experiments using native JavaScript api. 
Integration of this SDK into web application is easy, and its footprint is low.

This page describes the most basic `KameleoonClient` configuration, for more in-depth review of all the methods and configuration options follow [Official Kameleoon Documentation](https://developers.kameleoon.com/javascript-sdk.html)

## Contents
- [Installation](#installation)
- [Configuration](#configuration)

## Installation
- **npm** - `npm install @kameleoon/javascript-sdk`
- **yarn** - `yarn add @kameleoon/javascript-sdk`
- **pnpm** - `pnpm add @kameleoon/javascript-sdk`

## Configuration

1. Obtain your site code from [Kameleoon Platform](https://app.kameleoon.com/)
2. Create client instance
```ts
import { KameleoonClient } from '@kameleoon/javascript-sdk';

const client = new KameleoonClient('my_site_code');
```
3. Asynchronously initialize client to fetch the configuration from remote server and handle possible errors
```ts
try {
  await client.initialize();
} catch (error) {
  // Handle error
}
```
4. `KameleoonClient` is ready to go!
```ts
const visitorCode = KameleoonUtils.getVisitorCode('www.example.com');
const experimentId = 100;
const customDataIndex = 0;

// -- Get variation id
const variationId = client.triggerExperiment('my_visitor_code', experimentId);

// -- Add targeting data
client.addData(visitorCode, new CustomData(customDataIndex, 'my_data'));

// -- Check if the feature is active for visitor
const isMyFeatureActive = client.isFeatureFlagActive(
  visitorCode,
  'my_feature_key',
);
```


