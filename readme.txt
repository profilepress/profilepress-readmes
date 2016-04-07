=== ProfilePress ===
Contributors: Agbonghama Collins
Tags: login, registration, password reset, members, widget, users, profile, front-end profile, edit profile, avatar, profile picture
Requires at least: 4.0
Tested up to: 4.5
Stable tag: 2.3.1
License: GPL-2.0+

Ultimate User Manager plugin for WordPress.

== Description ==
Stupidly simple way to create user account forms without a single line of PHP code.

== Frequently Asked Questions ==
See the website for more info http://profilepress.net

== Changelog ==

= 2.3.1 =
* Fixed critical "header already sent" error.
* Added filter to disable plugin comment attribution in source code.
* Added ID to all form tags.
* Fixed a passwordless login bug.

= 2.3 =
* Fixed bug where profile avatar wasn't getting updated in edit profile form.
* Feature: explicitly make login form passwordless
* Added filter to skip passwordless login
* Composer autoloader for social login library.
* Fixed: bug where google login request offline access from users.
* Added multi selection for checkbox
* Added form ID to action hook after edit profile update
* Form builder UI enhancement.
* Added filter to all builder with missing error/status.
* Fixed: bug where a field with file upload wasn't selected in edit screen.
* Added filter to facebook and google social login scope.
* Fixed bug where output buffering caused unexpected white screen.
* All class instance are now loaded in plugins_loaded action

= 2.2.1 =
* Added limit to chose select multi option dropwdown.
* Fixed bug in multi-select dropwdown.
* Now using add_query_args function for social login links. 
* Added vk.com social login url shortcode.
* Fixed: Email confirmation not working when a melange form is use as login.

= 2.2 =
* Updated fzbuk forms css.
* Fixed bug where data weren't erased when an edit profile field is emptied.
* Added support for multiple option select dropdown.
* Fixed: duplicate creation of pages when plugin is deactivated and reactivated.
* Front-end profile now support nicename in profile url.
* Added VK.com social login.
* Added file size restrictions to file and avatar uploads.

= 2.1.3 =
* Turn off social login debug mode by default and added a filter to switch it ON if need be.
* Fixed metabox naming in welcome message settings.
* Fixed error when installing registration form theme.
* Fixed revision settings page conflicting with a theme options.php settings page.
* Fixed sanitization of custom field adding slash to quotes.
* Removed duplicate front-end profile settings


= 2.1.2 =
* Fixed bug where social login via Twitter doesn't use user's email address even when it is returned.
* Added filter for all shortcode attributes of form fields.

= 2.1.1 =
* Added option to disable required attribute in login and registration form fields.
* Fix issue where users' avatar/profile picture wasn't getting saved on front-end edit profile form

= 2.1 =
* Welcome message now triggers after registration via social login.
* Social login session is now destroyed when a user log out.
* Added filters to all login, registration, password reset and edit profile shortcodes.

= 2.0.1 =
* Fixed bug where users can't login with username when 'login with email' is activated
* Fixed small bug in flatui CSS.

= 2.0 =
* Added file uploader to custom field settings and implemented a class to handle the file uploads.
* Fixed "license key not activated" admin notice link to license settings page.
* Added user uploaded files to WordPress default profile page.
* Repositioned pp_after_Registration action hook after welcome message and before autologin
* Increased the gravatar size to about 300 to make the images legible.
* Added action hooks after social login and registration.
* fixed bug where Email Confirmation not working with option ‘Login with email’ enabled
* Restrict admin notices to only administrators.
* Added ability for user and admin to update file uploaded in WordPress default profile page.
* Added support to edit uploaded file in profilepress edit profile form.
* Added config to enable twitter to return user email only if app is whitelisted.
* Do not display number of pending user admin notice when its 0
* Added profile-file shortcode doc to contextual help tab

= 1.9.1 =
* Removed early escaping of user email address during password reset.
* Fixed facebook profile image not getting uploaded during social registration.
* Removed jquery dependence in datepicker script enqueue.
* Fixed multiple admin notification getting sent.
* Added filter to password reset error notice.
* Added filters to moderation notifications and welcome message after registration.
* Added admin notice when user registration is disabled.

= 1.9 =
* Added backward compatibility of password reset key generation harsh prior to WP 4.3
* Allows logged in users to reset their password.
* Made all admin notices dismissible.
* Added admin notification when a user registers an account.
* Added action hook to create custom shortcodes for forms and front-end profile.
* Added admin notice for user to add their license key when not activated.
* Check to see if pending_user role exist before adding the role to a user when moderation is active
* Fixed bug where user were lacking moderated role capability after approval.
* Added moderation capability to social login/registration.
* Added [pp-logged-users] and [pp-non-logged-users] shortcodes to make content visible to logged and non logged users respectively.
* Added custom url redirect capability for login and logout redirection.
* Added bulk user moderation.
* Refactored global redirection to include filter for custom page IDs.
* Fixed [pp-redirect-non-logged-in-users] shortcode redirecting to after_login_redirect_url instead of login page url.
* Added do reset password handler structure to theme installer.
* Added date field to registration and edit profile forms.
* Deleting a form now delete its revision.
* Added filter to alter stored revision count.
* User role selection baked into the registration form settings page.
* Added dashboard notification when a user is pending moderation.
* Added registration confirmation password field.
* Implemented password strength meter that can be added to registration form.

= 1.8.2 =
* Removed license activation restriction

= 1.8.1 =
* Fixed bug where admin user email notification include the string "time and season foods" instead of the site name. We're sorry.

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
