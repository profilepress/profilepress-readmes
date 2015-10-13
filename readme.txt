=== ProfilePress ===
Contributors: Agbonghama Collins
Tags: login, registration, password reset, members, widget, users, profile, front-end profile, edit profile, avatar, profile picture
Requires at least: 4.0
Tested up to: 4.3.1
Stable tag: 1.8
License: GPL-2.0+

Ultimate User Manager plugin for WordPress.

== Description ==
Stupidly simple way to create user account forms without a single line of PHP code.

== Frequently Asked Questions ==
See the website for more info http://profilepress.net

== Changelog ==

= 1.8.1 =
* Fixed bug where admin user email notification include the site name instead of the string "time and season foods". We're sorry.

= 1.8 =
* Fixed bug where passwordless email subject isn't set.
* Fixed bug with ProfilePress front-end profile title aving missing argument error.
* Refactored welcome email class and implementation.
* Added hook and filters to social signup register_user function.
* Fixed settings page design for adding new edit profile.
* Upgraded social login library.
* Added: Front-end password reset now possible.. hurray
* Change shortcake button id to class to enable multiple instance of wp-media window.
* Refactored user moderation approval class method.
* Added: send admin a notification when a user is pending approval and an approval link to approve users.
* Added filter to disable edit profile redirection to custom edit profile page for administrators.

= 1.7.2 =
* Fixed conflict with press permit plugin.
* Added option to disable passwordless login for site admins.
* fixed bug whereby sender name and email of password reset message defaulted to WordPress.
* Fixed username not being included in passeordless login email to user.
* More code improvement.

= 1.7.1 =
* Fixed bug when displaying user profile with space in username.
* Removed network_admin_menu from melange settings page
* Added blog_id to melange table on multisite DB creation
* Fixed bug with plugin not creating custom tables during multisite installation.
* Added action link below user to send one time passwordless login link
* Increased custom profile fields options from 200 chars to 3000

= 1.7 =
* fixed password reset key being invalid.
* Reduced the time in seconds before temp user created by social login for WPengine supported host is deleted
* Removed user password from welcome message on plugin activation
* Removed deprecated pp_extras_page filter in extras settings page
* Changed avatar folder to a folder called 'pp-avatar' in wp-content
* Ensure temp user during social login is deleted when authorization is cancelled or trigger an error.
* Fixed shortcode tags in html link made broken by WordPress 4.3 release change in shortcode API

= 1.6.1 =
* Added WPEngine(and host without PHP session) support for social login.
* Fixed a small bug in profilepress avatar implementation.
* Added bbPress and buddyPress plugin integration: override both profiles urls with ProfilePress front-end profile.

= 1.6 =
* Added filter to change front-end profile slug
* Added support for sortable of profile fields
* Fixed multisite problem causing 500 internal server error.
* Removed network_admin_menu from plugin
* Improve plugin uninstallation for multisite
* Fixed invalid translation function

= 1.5.4 =
* Removed action attribute from form tags
* Fixed restoring revision of melange
* Extended the number of characters in melange title to 50.
* auto login after registration now work even if user moderation is enabled.
* Make front-end profile shortcode available outside of front-end profile builder.

= 1.5.3 =
* Fix user login bug due to unnecessary captcha verification when recaptcha is inactive.

= 1.5.2 =
* Fix misplaced argument in "pp_after_registration" Action.

= 1.5.1 =
* Fix password reset link getting overriden by WooCommerce and similar plugins.
* Fix Javascript security issue in recaptcha when js is disabled.
* Include registered user ID to "pp_after_registration" filter.

= 1.5 =
* Fixed: multiple instance of reCAPCHA resource link in header.
* Added: PANTHEON hosting session support.
* Added: Ability to redirect users to the page they were before they logged in.
* New filters: pp_extras_page_top and pp_extras_page_bottom.
* Removed: obnoxious license expired admin notice.
* Updated: TGM activation class.
* Added: new front-end profile called Monochrome.
* Improved plugin translation and internalization.

= 1.4.2 =
* Hot Fix: missing argument in auto login function call.
* Prefixed all ProfilePress CSS and JS components.

= 1.4.1 =
* Hot Fix: undefine BP function call.

= 1.4 =
* Added: support for BuddyPress.

= 1.3.4.1 =
* Fixed: error when user is logged out.

= 1.3.4 =
* Fixed: Linkedin social login.
* Added: filter for login and logout url redirect.

= 1.3.3 =
* Added: textarea custom field for registration and edit profile.
* Added: support for any form field attribute be it tabindex, size, maxlength etc.

= 1.3.2 =
* Fixed: bug in PP SQL that prevented custom field from being deleted.

= 1.3.1 =
* Fixed: Global redirect error causing login, registration and password reset page to be affected by the redirect.

= 1.3 =
* Mew: Added Melange combo form builder.
* New: Global ite redirect.
* New: Improvement in plugin translation (60% done).
* Bug fixes and tweaks.

= 1.2.1 =
* UI improvement.
* Big feature: Revision. Rollback to a previously saved design effortlessly. 

= 1.1.1 =
* Added new filters for addons settings.
* Few bug fixes and improvement.

= 1.1.0 =
* Added redirect attribute to login and registration shortcodes.

= 1.0 =
* the genesis.
