=== License Manager for WooCommerce ===
Contributors: drazenbebic
Donate link: https://www.licensemanager.at/donate/
Tags: license key, license, key, software license, serial key, manager, woocommerce, wordpress
Requires at least: 4.7
Tested up to: 5.4
Stable tag: 2.2.0
License: GPLv3
License URI: https://www.gnu.org/licenses/gpl-3.0.html

Easily sell and manage software license keys through your WooCommerce shop

== Description ==
The **License Manager for WooCommerce** allows you to easily sell and manage all of your digital license keys. With features like the bulk importer, automatic delivery, and database encryption, your shop will now run easier than ever.

[Plugin & API Documentation](https://www.licensemanager.at/docs)

#### Key plugin features

* Automatically sell and deliver license keys through WooCommerce
* Manually resend license keys
* Add a single license key and assign it to a specific product
* Add multiple license keys (by file upload) and assign them to a specific product
* Export license keys as PDF or CSV
* Manage the status of your license keys
* Create license key generators with custom parameters
* Assign a generator to one (or more!) WooCommerce product(s), these products then automatically create a license key whenever they are sold

#### API

The plugin also offers additional endpoints for manipulating licenses and generator resources. These routes are authorized via API keys (generated through the plugin settings) and accessed via the WordPress API. An extensive [API documentation](https://www.licensemanager.at/docs/rest-api/v2/) is also available.

#### Support

If you have any feature requests, need more hooks, or maybe have even found a bug, please let us know in the support forum or e-mail us at <support@licensemanager.at>. We look forward to hearing from you!

You can also check out the [documentation pages](https://www.licensemanager.at/docs/handbook/), as they contain the most essential information on what the plugin can do for you.

#### Important

The plugin will create two files inside the `wp-content/uploads/lmfwc-files` folder. These files (`defuse.txt` and `secret.txt`) contain cryptographic secrets which are automatically generated if they don't exist. These cryptographic secrets are used to encrypt, decrypt and hash your license keys. Once they are generated please **back them up somewhere safe**. In case you lose these two files your encrypted license keys inside the database will remain forever lost!

== Installation ==

#### Manual installation

1. Upload the plugin files to the `/wp-content/plugins/license-manager-for-woocommerce` directory, or install the plugin through the WordPress *Plugins* page directly.
1. Activate the plugin through the *Plugins* page in WordPress.
1. Use the *License Manager* → *Settings* page to configure the plugin.

#### Installation through WordPress

1. Open up your WordPress Dashboard and navigate to the *Plugins* page.
1. Click on *Add new*
1. In the search bar type "License Manager for WooCommerce"
1. Select this plugin and click on *Install now*

#### Important

The plugin will create two files inside the `wp-content/uploads/lmfwc-files` folder. These files (`defuse.txt` and `secret.txt`) contain cryptographic secrets which are automatically generated if they don't exist. These cryptographic secrets are used to encrypt, decrypt and hash your license keys. Once they are generated please **back them up somewhere safe**. In case you lose these two files your encrypted license keys inside the database will remain forever lost!

== Frequently Asked Questions ==

= Is there a documentation? =

Yes, there is! An extensive documentation describing the plugin features and functionality in detail can be found on the [plugin homepage](https://www.licensemanager.at/docs/).

= What about the API documentation? =

Again, yes! Here you can find the [API Documentation](https://www.licensemanager.at/docs/rest-api/v2/) detailing all the new endpoint requests and responses. Have fun!

== Screenshots ==

1. The license key overview page.
2. Add a single license key.
3. Add multiple license keys in bulk.
4. WooCommerce simple product options.
5. WooCommerce variable product options.
6. The generators overview page.
7. Create a new license key generator.

== Changelog ==

= 2.1.2 - 2019-12-09 =
* Add - The plugin now checks the PHP version upon activation. If the version is on/below 5.3.29, the plugin will not activate.
* Add - `lmfwc_event_post_order_license_keys` event action has been added. You can hook-in with the `add_action()` function.
* Fix - Removed the "public" properties from the class constants.
* Fix - Column screen options now work for the license and generator pages.
* Fix - Timestamps are now properly converted and displayed on the licenses page.

[See changelog for all versions](https://raw.githubusercontent.com/drazenbebic/license-manager-for-woocommerce/master/CHANGELOG.md).

== Upgrade Notice ==

= 1.2.1 =
Please deactivate the plugin and reactivate it.

= 1.1.1 =
Copy your previously backed up `defuse.txt` and `secret.txt` to the `wp-content/uploads/lmfwc-files/` folder. Overwrite the existing files, as those are incompatible with the keys you already have in your database. If you did not backup these files previously, then you will need to completely delete (not deactivate!) and install the plugin anew.

= 1.0.0 =
There is no specific upgrade process for the initial release. Simply install the plugin and you're good to go!