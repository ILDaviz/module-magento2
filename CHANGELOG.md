# Changelog

## [0.32.0] - 2020-04-08
### Added
- Add an option to cancel import for new marketplace orders
- Add an "Importable" column to the marketplace order listing
- Add missing french translations

### Fixed
- Regularly update the status of unimported marketplace orders

## [0.31.0] - 2020-03-26
### Added
- Add an option to import order customers (**BC break** for sales order importer)
- Implement dynamic rows config fields

### Changed
- Improve the handling of regions for some countries
- Replace hard-coded class names in error messages

## [0.30.1] - 2020-03-23
### Fixed
- Fix handling of some of the cart conditions in shipping method rules

## [0.30.0] - 2020-03-06
### Added
- Add an option to choose the product types to export
- Implement export for virtual products
- Add an option to choose how to export base and discount prices

### Fixed
- Fix compatibility with PHP 7.4

## [0.29.0] - 2020-02-28
### Added
- Add more notes/feedback in the account configuration form
- Add an option to check product websites when importing orders
- Add a "pattern" column to the shipping method rule listing

### Changed
- Improve the rendering of notes in the account configuration form

### Fixed
- Fix the translation of save buttons
- Fix some button/field labels in the cron task form
- Fix the basic shipping method applier with codes containing multiple underscores

## [0.28.1] - 2019-12-17
### Fixed
- Fix mass-update tab on recent M2 versions

## [0.28.0] - 2019-12-16
### Added
- Improve the feed product listing:
    - Add new attribute columns (type, status, visibility, price)
    - Add new feed columns (main and variation states, exclusion reason)
    - Add a sections details modal
- Implement mass-update for those product attributes: is selected, forced category
- Add an option for fetching different types of quantities when using MSI
- Implement utility methods for shipping method appliers

### Fixed
- Fix import of orders with disabled products (with or without availability check)

## [0.27.0] - 2019-12-04
### Added
-	Fetch product quantities using MSI (if available) (**BC break** for stock section adapter)

## [0.26.0] - 2019-10-31
### Changed
- Refactor shipping method appliers and improve defaults (**BC break** for custom shipping method appliers)

### Fixed
- Exclude the "All Groups" group from the options available in "Use Prices from Customer Group"
- Fix the "Category Selection" label on recent M2 versions

## [0.25.2] - 2019-10-07
### Added
- Add a details column to the order logs listing

### Fixed
- Fix usages of table codes instead of table names

## [0.25.1] - 2019-09-19
### Fixed
- Fix memory overflow with large catalogs when exporting an empty feed

## [0.25.0] - 2019-09-10
### Added
- Allow specifying a customer group with which to fetch product prices
- Import marketplace fees for orders

### Fixed
- Fix feed URL in account listing when using gzip
- Fix wrong table name used for configurable product attributes
- Force frontend config scope when executing CLI commands

## [0.24.0] - 2019-08-26
### Added
- Add an option for selecting exportable products using a custom attribute

### Changed
- Refactor attribute sources

## [0.23.1] - 2019-08-21
### Changed
- Improve prevention of stock checks when not in admin scope

## [0.23.0] - 2019-08-08
### Changed
- Remove final keywords from functions
- Improve generation of unique feed filenames

## [0.22.1] - 2019-08-01
### Added
- Import the company in order addresses
- Allow partial refunds on imported orders

### Changed
- Only fetch marketplace orders waiting shipment

### Fixed
- Fix ACL and menu configuration

## [0.22.0] - 2019-07-11
### Added
- Add new columns to the marketplace order listings
- Detect SKUs when using product IDs for order import

### Changed
- Improve default phone number handling
- Improve prevention of duplicate order import in some edge cases
- Improve prevention of stock checks for Magento 2.3

## [0.21.0] - 2019-07-03
### Added
- Add ability to create a new Shopping Feed account

### Changed
- Bump order import try count earlier
- Rework account/store management and UI

### Fixed
- Fix the "partially shipped" order status constant
- Fix french translation for "Use item reference [..]"
- Remove explicit proxies from constructors

## [0.20.0] - 2019-05-07
### Added
- Fetch the tax amount for marketplace order items

### Changed
- Bumped `shoppingfeed/php-sdk` dependency from **0.2.4** to **0.2.6**
- Improve the detection of untaxed (business) orders

### Fixed
- Fix rendering for options-based attributes with non-text labels

## [0.19.0] - 2019-04-24
### Fixed
- Fix compatibility problems with Magento 2.1.x

## [0.18.0] - 2019-03-27
### Added
- Add "price_before_discount" and "shipping_delay" attributes to the feed

### Changed
- Force cross border trade when importing orders (togglable off)

## [0.17.1] - 2019-03-21
### Fixed
- Fix ambiguous filters in the orders listing
- Fix export of product variations in some edge cases

## [0.17.0] - 2019-03-11
### Fixed
- Fix the capacity of the Shopping Feed order ID field

## [0.16.0] - 2019-03-05
### Added
- Add explicit dependency to Guzzle

## [0.15.0] - 2019-02-26
### Added
- Handle WEEE attributes at feed export and orders import

## [0.14.1] - 2019-02-04
### Changed
- Improve the detection of product quantity changes

## [0.14.0] - 2019-01-30
### Added
- Add marketplace fields to the sales order listing
- Add the marketplace shipping and payment methods to the available conditions for shipping method rules
- Implement real-time updates for product quantities

### Changed
- Do not check product availability and options by default
- Refactor store configuration management
- Filter on active shipping method rules when importing orders

### Fixed
- Fix the orders listing (wrong join type)
- Fix the order import "super mode" on newer M2 versions

## [0.13.1] - 2019-01-02
### Fixed
- Fix order address import

## [0.13.0] - 2018-12-19
### Changed
- Import business orders without tax

### Fixed
- Fix updates batching when products retention is enabled
-  Fix translations

## [0.12.2] - 2018-12-18
### Added
- Add ability to export the attribute set name in the feed

### Fixed
- Fix initialization of timestamp fields in DataObjects
- Fix filtering on Magento # in marketplace orders listing

## [0.12.1] - 2018-12-14
### Removed
- Remove composer dependencies for packagist version

## [0.12.0] - 2018-12-14
### Added
- Register dependencies in module sequence and composer.json

### Changed
- Emulate the CLI area code rather than setting it
- Wrap "sensitive" types (wrt loading order) in proxies
- Fill missing required address fields with sensible and/or user defaults

### Fixed
- Fix translations

## [0.11.0] - 2018-12-11
### Added
- Add the listing of order logs to the sales menu

### Changed
- Fill the first name in marketplace addresses when unavailable
- Only try to import unshipped accepted orders
- Only fetch recent marketplace orders

## [0.10.0] - 2018-12-10
### Fixed
- Fix shipment syncing and SF ticket handling

## [0.9.2] - 2018-12-10
### Fixed
- Fix shipment syncing

## [0.9.1] - 2018-12-06
### Added
- Allow to use mobile phone number first for imported order addresses

## [0.9.0] - 2018-12-05
### Added
- Add ability to synchronize addresses with SF for fetched orders not imported yet

### Fixed
- Complete/fix french translations
- Fix indentation quirks
- Fix Magento # column in marketplace orders listing

## [0.8.0] - 2018-11-21
### Added
- Implement forced refresh for updated products only
- Implement price export for configurable products

### Changed
- Improve determination of category URLs

### Fixed
- Fix default cron task setup
- Fix account creation (only existing accounts are allowed for now)
- Fix parent products export in some rare cases

## [0.7.0] - 2018-11-06
### Added
- Force feed refresh in case of meaningful configuration change

### Changed
- Bumped `shoppingfeed/php-feed-generator` dependency from **1.0.0** to **1.0.2**
- Tweak various constants (database / UI)

### Fixed
- Fix product lists syncing after product save

## [0.6.0] - 2018-10-29
### Added
- Add a success message upon running a cron task
- Implement batched updates for feed data
- Add "Store View" column to account store listing
- Add the product URL to the attributes section data
- Add the platform information to the API client

### Changed
- Clean up code

### Fixed
- Fix french translations
- Fix feed refresh (force using the relevant store view + use batched updates)

## [0.5.0] - 2018-10-23
- Initial release
