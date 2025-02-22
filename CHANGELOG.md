# Change Log

All notable changes to this project will be documented in this file.

[Project Homepage](https://developers.kameleoon.com/javascript-sdk.html)

# 1.5.2 (2023-07-17)


### Bug fixes

- Typescript `.d.ts` files have proper relative path resolution.

# 1.5.1 (2023-06-30)


### Bug fixes

* Tracking data duplications

# 1.5.0 (2023-06-28)


### Bug fixes

- Improve error handling for [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api)
- Visitor code is now validated correctly in every method that uses it.
- Result bundle is now compatible with systems not using `ESM` and `CommonJS`. It's minimized and uses code splitting for `crypto-js` `sha256` function.
- Parameter `revenue` for [`Conversion`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#conversion) is now optional.
- Each visitor can now only have one type of associated [`Kameleoon Data Type`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#data-types), except for [`CustomData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#customdata), that a visitor can have one per `customDataIndex`.

### Features

- New conditions are now supported: `Device`, `Browser`, `SDKLanguage`, `Page Title`, `Page View`, `Visitor Code`, `Conversion`. See the [full list of supported conditions](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#list-of-supported-targeting-conditions).
- [`Browser`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#browser) now has new optional parameter `version`.
- [`flushData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#flush-tracking-data) `visitorCode` parameter is now optional.
- Custom data that is marked as `local only` on Kameleoon Platform is now only used for targeting (not flushed with tracking requests).
- JavaScript SDK is now available as a single file from the static server, see the [details](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#installation)


# 1.4.4 (2023-06-01)


### Bug fixes

* Empty visitor code is no more allowed
* Incorrect tracking body upon triggering an experiment

# 1.4.3 (2023-05-24)


### Bug fixes

* Fixed issue for sending unique `Nonce` parameter on tracking requests

# 1.4.2 (2023-05-21)


### Bug fixes

* [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api) current visits not being up-to-date

# 1.4.1 (2023-05-20)


### Bug fixes

* [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api) data parse error

# 1.4.0 (2023-05-19)


### Features

* Added method [`getRemoteVisitorData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#obtain-custom-data-from-kameleoon-data-api)
* Added offline mode for [`initialize`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#initialize-kameleoon-client) method.

# 1.3.3 (2023-05-16)


### Bug fixes

* Initialization throws error

# 1.3.2 (2023-04-24)


### Bug fixes

* Tracking feature flag rule with variation `off` wasn't displayed on result page

# 1.3.1 (2023-04-22)


### Bug fixes

* core dependency fix

# 1.3.0 (2023-04-21)


### Features

* Added method [`getEngineTrackingCode`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#sending-exposure-events-to-external-tools)

# 1.2.0 (2023-04-14)

### Features

* Added method [`getExperimentVariationData`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#get-experiment-variation-data)
* Targeting data cleanup interval is now [`optional`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#1-initializing-the-kameleoon-client) and not set by default
* [`getFeatureFlagVariationKey`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#get-variation-key-for-a-certain-feature-flag), [`getFeatureFlagVariable`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#get-a-variable-of-a-certain-feature-flag), [`isFeatureFlagActive`](https://developers.kameleoon.com/feature-management-and-experimentation/web-sdks/js-sdk#check-if-the-feature-is-active-for-visitor) methods do not check previously allocated variation, rather recalculate it each time. Same methods now send tracking request for any rule type (previously only for `Experementation` rule)

### Bug fixes

* `variationId` is undefined when using feature flag related methods

# 1.1.1 (2023-04-05)


### Bug fixes

* Internal bug fixes

# 1.1.0 (2023-03-22)


### Features

- License changed from `GPL3.0` to `ISC`


# 1.0.0 (2023-03-21)


### Features

* Initial Release
