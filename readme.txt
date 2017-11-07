=== ProfilePress ===
Contributors: Collins Agbonghama
Tags: login, registration, password reset, members, widget, users, profile, front-end profile, edit profile, avatar, profile picture
Requires at least: 4.0
Tested up to: 4.9
Stable tag: 2.9
License: GPL-2.0+

Ultimate WordPress plugin for User Registration, Login, Profile & more.

== Description ==
Stupidly simple way to create WordPress user registration, login, password reset forms as well as user profile without a single line of PHP code.

ProfilePress is the ultimate WordPress user management plugin.

== Frequently Asked Questions ==
See the website for more info https://profilepress.net

== Changelog ==

= 2.9 =
* Comment count profile shortcode now return only empty comment_type. Thus removing removing EDD and WooCommerce order notes.
* Fixed bug where clicking on password reset link on site without pretty permalink was failing.
* Fixed bug where [user-avatar-url] was returning html image of user profile avatar instead of just the url.
* Ensure user object variable is set to prevent undefined variable error throwing when WP_Debug is true.
* Added more parameters to pp_before_saving_file and pp_after_saving_file hooks.
* Upgraded hybridauth and Facebook PHP SDK which apparently fix issues with Facebook login.
* User moderation now kicks in during social login only if moderation is active.
* Added default select option to "after password reset" redirect.
* Password reset and handler forms now hidden after successful reset. The former doesn't get hidden in non-ajax mode. Sorry!
* Changing of user profile slug now possible in settings.
* Metabox handle icon now displays for visibility toggling.
* Added expand and collapse buttons to general settings page.
* BbPress and BuddyPress settings now only show up if their plugins are active.
* Added password strength meter shortcode to edit profile form.
* Added "pp_min_password_strength" filter to reduce password minimum strength requirement in supported forms.
* Fixed bug where cloning a registration form displayed cloned role as date and date as role.

= 2.8.8 =
* Added filter to disable/modify google captcha script.
* Added filter to make content-type of 'pending user admin notification email' HTML.
* Added filter to disable flatui and bootstrap CSS stylesheets.
* Added new [profile-post-list] shortcode to display list of user posts.
* Fixed bug where redirection to current page after login wasn’t working in Ajax mode.
* Added user profile title rewrite support to themes using add_theme_support( 'title-tag’) for core to output title in pages.
* Frontend profile shortcode now accept "user-id" to display profile info of any specific user.
* Added shortcode to display date users registered.
* Fixed bug where pending user admin notice cause settings page not to display.
* Fixed bug where empty password reset subject and/or body could cause reset email not to be sent.

= 2.8.7 =
* Entered username/email address during password reset is now cleared after every reset attempt.
* Login form without 'remember me' checkbox default to long expiring session.
* Code and performance improvements.

= 2.8.6 =
* Fixed bug that prevented plugin updates from being received.

= 2.8.5 =
* Added more filter to wp_email admin email addresses
* pp_site_url_without_scheme() now return just the host address even if the wordpress install is in e.g domain.tld/wp
* Bail if sender email is not valid. Hoping this will reduce support tickets about ajax registration breaking.
* Fix small bug in invalid object reference in avatar class

= 2.8.4 =
* Added support for redirect attribute in melange edit profile / edit profile form.
* Added "option to redirect to page /url after successful password reset".
* Fixed bug in login PHP class that broke tabbed login/sign up/ lost password widget.
* Added {{block_url}} placeholder for admin to block new user after registration right inside the email.
* Fixed issue with 'new user notification not sending'.
* Added agreeable custom field.
* Added cloning feature to form builder listing page.
* Fixed bug where pp_chosen_browser_is_supported() function is undefined in form preview frame. hence breaking the preview onload.

= 2.8.3 =
* Fixed jquery chosen bug deselection on desktop.
* Improve responsiveness of profilepress core themes.
* Fixed bug where signup from melange wasn't shown in "Registered Via" column in user listing.
* Added filter to admin email that will receive new user notification.
* Added filter to password reset subject and message.
* Added more filters to front end profile and action to settings form parser.

= 2.8.2 =
* Fixed bug where value of "redirect_to" query string wasn't being used after ajax login is successful in ProfilePress powered login form.
* Fixed bug where select limit of last select-dropdown affects the preceded ones.
* Added support for limiting selectable options in multiselect custom field for mobile devices.
* Fixed bug where plugin admin css wasn't enqueued in certain critical areas.

= 2.8.1 =
* Added filter "pp_allow_empty_password_unchanged" to edit profile form. if set to true, empty password and empty confirm password field will cause password not to be changed.
* Made default login redirect to ProfilePress custom login page WordPress core compliant by adding "redirect_to" when redirecting.
* Listing of custom fields under "other information" in profile admin page now exclude all woocommerce core billing and shipping fields.
* Added redirect attribute support to melange login form.

= 2.8 =
* Added checkbox for disabling of user status email notification.
* Added password, email, tel, hidden, country and number custom fields.
* Fixed bug where site.com/wp-admin wasn't redirecting to set custom login page.
* Added firstname and lastname fields to 'new user admin notification settings.
* Fixed bug with validating required fields in checkbox, radio, select.
* Redirect to currently viewed page on social login now working.
* Fixed bug where empty field in new user admin notification settings could break (ajax) registration.
* Added confirm password field to edit profile form.
* added filters to wp_insert_user() call.

= 2.7.1 =
* Fixed potiential issue where license control class unavailability could break admin ajax.

= 2.7 =
* Added email confirmation field to edit user profile form.
* Improved license activation, deactivation and updater.
* Added {{email}} placeholder to passwod reset message content.
* Fixed issue where login via email address result in username being show as login identifier when there is login error.
* Added filter to enable remember me in passwordless login. 
* Fix bug where forward slash was being added to single quoted value of custom field.
* Added [password-hint] shortcode to display hint on generating better and stronger password.
* Add placeholder to include link to reset password in welcome message.
* Added filters to moderation notification and passwordless login placeholders.
* Added email placeholder to welcome message and filter to include custom placeholders.
* Fixed issue of multiple status message/notice being display after editing profile in ajax mode.
* Added confirm email field to registration form.
* Added server-side validation of required fields.
* Added (more) validation to custom field settings page.
* Simplified logic for adding required attribute to fields.
* Plugin admin css and js now loaded only in ProfilePress settings pages.
* Added filter to disable pending user admin notification.
* Added email placeholder to moderation status email notifications.
* Added first name and last name placeholder for "Admin Notification When a New User Is Pending Approval" notification.
* Added filter to success and error message.
* Fixed error 'TypeError: invalid ‘in’ operand response' when trying to login and signup when user is already logged in.
* Added email address validation when editing profile.

= 2.6.2 =
* Fixed bug where social login resulted to whitepage being displayed.

= 2.6.1 =
* Bug fixes in frontend.js
* Removed shortcake "Add Post Element" button.
* Fixed bug where disable ajax mode notice displays even when disabled.
* Fixed bug where contact info wasn't added because of contact-info query string being cleared.
* Custom profile field key limit has been upgraded to 100.
* Updated google fonts to https in all ProfilePress themes.
* Fixed php error display in checkbox options in edit profile form.
* Fix bug where empty checkboxes do not return value in POSTed data.
* Added "disable username requirement" support to melange.
* Fixed bug in GitHub username detection on social login.
* Username generation via facebook social login now from the username part of their email addresses.
* Using one central composer autoloader.

= 2.6 =
* Added detection of admin ssl flag during login via autologin, passwordless login and social login.
* Added filter to disable redirect from default wordpress account form to custom one.
* Fixed bug where disable ajax mode notice displays even when disabled.
* If password form field is empty, a link to reset password reset is sent immediately after user registration.
* Added hook to dismiss ajax enabled notification.
* Added: no-login-redirect attribute to registration shortcode to redirect user to custom page after registration without autologin.
* Added: "pp_auto_login_before_signup_redirection" filter to disable autologin in "autologin after registration module" before redirecting to custom url after registration.
* Improve support for melange forms in ajax mode.
* ProfilePress avatar now overrides that of buddypress.
* Added shortcode pp-redirect-logged-in-users.
* Social signup now trigger new user notification sent to admin.
* Heartbeat auth check now return default WordPress login page instead of ProfilePress powered login page.
* Responsive fix for all Smiley themes.
* Added: customization of "new user notification to admin" email now possible.
* Added filter to deactivate tgmpa admin notice.
* Added indicator to show where user signup from.
* Added checkbox to disable username requirement in registration form admin screen.
* Bug fixes in form builders settings pages.
* Registration without username now possible when it checkbox settings is checked.
* Social login library upgrade.

= 2.5.6 =
* Added filter to disable 'registration disable admin notice'
* New: if password reset field isn't present in registration form, random password is generated and password reset triggered for users to reset their password.
* Added password strength meter to do password reset form.
* Bug fixes and code improvement to support polylang extension.

= 2.5.5 =
* Fixed bug where setting admin dashboard to SSL causes logging in to WordPress feature to fail.

= 2.5.4 =
* Added filter to login, registration, password reset and edit profile form tag
* Fixed bug where license is deem invalid after check. now it can update license status
* Remove some shipped bootstrap css bloat
* Added event triggering in various stages of ajax mode of forms
* Added ajax support to melange form
* Fixed mixed content warning in console for Rye google font css import rule
* Added some action hook to support buddypress profile sync addon


= 2.5.3 =
* Fix critical bug where resetting of password was failing.

= 2.5.2 =
* Fix irregular nonce security failure on ajax login, registration and password reset forms.

= 2.5.1 =
* Fixed bug where action and filter callbacks where not triggering in Ajax mode.
* PHP 7 ready. Hurray!!!

= 2.5 =
* New: Ajaxification of login forms.
* New: Ajaxification of registration forms.
* New: Ajaxification of password reset forms.
* New: Ajaxification of tabbed widgets.
* New: Ajaxification of widgets forms.
* Performance and code improvements.
* Few bug fixes.

= 2.4.1 =
* Fixed dashboard error displayed related to accessing an array that turns out to be a boolean
* Fixed bug where user password was cleared when the password field is empty thus logging them out
* Added check for DOING_AJAX
* Fixed critical bug in user registration form

= 2.4 =
* Moved avatar validation before actual user registration.
* New: added registration shortcode that display a list of roles user can choose on registration.
* Fixed bug where global multisite form where restricted to blog_id that made the form update.
* Fixed bug where new edit profile form wasn't being added to database.
* New: added user panel widget.
* New: added "pp-hide-empty-field" shortcode to hide profile field when it has no value or its empty.
* New: shortcodes for bbpress specific profile links eg topic created, subscriptions etc.
* New: buttons to install starter themes for login, registration, password reset, edit profile and front-end user profile.
* Hardening of plugin securityin light of ninja form exploit.
* Bug fixes and tweaks.

= 2.3.2 =
* Fixed bug where avatar upload on registration and edit profile forms not working correctly.

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
