# Changelog DeviceRoamingStatus

<!-- TOC:START -->
## Table of Contents
- [r2.1](#r21)
<!-- TOC:END -->

**Please be aware that the project will have frequent updates to the main branch. There are no compatibility guarantees associated with code in any branch, including main, until it has been released. For example, changes may be reverted before a release is published. For the best results, use the latest published release.**

The below sections record the changes for each API version in each release as follows:

* for an alpha release, the delta with respect to the previous release
* for the first release-candidate, all changes since the last public release
* for subsequent release-candidate(s), only the delta to the previous release-candidate
* for a public release, the consolidated changes since the previous public release

# r2.1

## Release Notes

This release candidate contains the definition and documentation of
* device-roaming-status-subscriptions 0.9.0-rc.1
* device-roaming-status 1.2.0-rc.3

The API definition(s) are based on
* Commonalities 0.8.0
* Identity and Consent Management 0.5.0

## device-roaming-status-subscriptions 0.9.0-rc.1

**device-roaming-status-subscriptions 0.9.0-rc.1 is a release-candidate version of this API.**

Changes documented below are compared to version 0.8.0.

- API definition **with inline documentation**:
  - [View it on ReDoc](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/camaraproject/DeviceRoamingStatus/r2.1/code/API_definitions/device-roaming-status-subscriptions.yaml&nocors)
  - [View it on Swagger Editor](https://camaraproject.github.io/swagger-ui/?url=https://raw.githubusercontent.com/camaraproject/DeviceRoamingStatus/r2.1/code/API_definitions/device-roaming-status-subscriptions.yaml)
  - OpenAPI [YAML spec file](https://github.com/camaraproject/DeviceRoamingStatus/blob/r2.1/code/API_definitions/device-roaming-status-subscriptions.yaml)

### Breaking changes

* Update API definitions to fix CAMARA validation warnings and hints by @eric-murray in https://github.com/camaraproject/DeviceRoamingStatus/pull/78
  - Pagination for listing of subscriptions using GET /subscriptions is now supported
    -  Addition of `page` and `perPage` query parameters to control pagination
    -  Returned subscriptions are now embedded in the array `subscriptions` within the response JSON, with the page tracked within the `pagination` JSON
    -  Addition of response headers `X-Total-Count`, `X-Total-Pages` and `Link` to facilitate page navigation

### Added

* Add examples for roaming status retrieval by @bigludo7 in https://github.com/camaraproject/DeviceRoamingStatus/pull/53

### Changed

* Update API definitions to fix CAMARA validation warnings and hints by @eric-murray in https://github.com/camaraproject/DeviceRoamingStatus/pull/78
  - Pagination for listing of subscriptions using GET /subscriptions is now supported
    -  Addition of `page` and `perPage` query parameters to control pagination
    -  Returned subscriptions are now embedded in the array `subscriptions` within the response JSON, with the page tracked within the `pagination` JSON
    -  Addition of response headers `X-Total-Count`, `X-Total-Pages` and `Link` to facilitate page navigation

### Fixed

* fix: declare CloudEvent schema type by @hdamker in https://github.com/camaraproject/DeviceRoamingStatus/pull/77
* Fix example for Network Access Identifier by @bigludo7 in https://github.com/camaraproject/DeviceRoamingStatus/pull/58

### Removed

* Delete redundant API Readiness Checklists by @eric-murray in https://github.com/camaraproject/DeviceRoamingStatus/pull/82

## device-roaming-status 1.2.0-rc.3

**device-roaming-status 1.2.0-rc.3 is a release-candidate version of this API.**

Changes documented below are compared to version 1.1.0.

- API definition **with inline documentation**:
  - [View it on ReDoc](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/camaraproject/DeviceRoamingStatus/r2.1/code/API_definitions/device-roaming-status.yaml&nocors)
  - [View it on Swagger Editor](https://camaraproject.github.io/swagger-ui/?url=https://raw.githubusercontent.com/camaraproject/DeviceRoamingStatus/r2.1/code/API_definitions/device-roaming-status.yaml)
  - OpenAPI [YAML spec file](https://github.com/camaraproject/DeviceRoamingStatus/blob/r2.1/code/API_definitions/device-roaming-status.yaml)

### Breaking changes

* N/A

### Added

* N/A

### Changed

* Clarify LastStatusTime schema description in YAML by @eric-murray in https://github.com/camaraproject/DeviceRoamingStatus/pull/56
* Update API definitions to fix CAMARA validation warnings and hints by @eric-murray in https://github.com/camaraproject/DeviceRoamingStatus/pull/78

### Fixed

* Fix example label: Multiple Country Codes → Multiple Country Names by @sachinvodafone in https://github.com/camaraproject/DeviceRoamingStatus/pull/54
* Fix example for Network Access Identifier by @bigludo7 in https://github.com/camaraproject/DeviceRoamingStatus/pull/58

### Removed

* Delete redundant API Readiness Checklists by @eric-murray in https://github.com/camaraproject/DeviceRoamingStatus/pull/82

**Full Changelog**: https://github.com/camaraproject/DeviceRoamingStatus/compare/r1.2...r2.1

