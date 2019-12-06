# 4.3.4 (30 Oct 2019)

* [*] Internal security improvements.

# 4.3.3 (25 Oct 2019)

* [-] Daily maintenance script will no longer put garbage messages in `panel.log` on Plesk Onyx 17.5. (EXTWPTOOLK-3773)

# 4.3.2 (24 Oct 2019)

* [+] Smart Updates now use an new algorithm for analyzing plugin shortcodes, which should address most (if not all) false positives.
* [*] Improved support for Move Domains feature in Plesk Obsidian.
* [*] Smart Updates will warn user if a Smart Update procedure failed due to specific .htaccess customizations.
* [*] Smart Updates sitemap analysis was optimized to increase reliability.
* [-] Screenshot previews in the email notifications about Smart Update results are now displayed properly. (EXTWPTOOLK-3161)
* [-] Caching operations were optimized to address performance issues happening in certain cases with Plesk search and WordPress Toolkit site list. (EXTWPTOOLK-3567)
* [-] Smart Updates will now properly work if sitemap of the cloned website differs from the original due to meddling of certain plugins. (EXTWPTOOLK-3611)
* [-] Handling of nginx config files was changed to address the `Unable to reconfigure domain` error happening under certain circumstances. (EXTWPTOOLK-3626)
* [-] `Sort` control now works properly in the `Security Status` window. (EXTWPTOOLK-3609)
* [-] Smart Updates will not process unnecessary locations from XML sitemaps anymore. (EXTWPTOOLK-3610)
* [-] Smart Updates can now work with websites locally accessible only via domain aliases. (EXTWPTOOLK-3613)
* [-] Certain operations under certain conditions were failing with `Event not scheduled` error. Scheduling certain events was certainly improved to handle this. (EXTWPTOOLK-3616)
* [-] Unsolicited jumping of input focus happening in some cases was removed from the `Clone` window. (EXTWPTOOLK-3633)

# 4.3.1 (03 Oct 2019)

* [+] Cloning and Smart Updates now support websites with permalinks working on nginx.  
* [*] WordPress Toolkit now spotlights 1 month free trial for Smart Updates to server administrators.
* [*] WordPress Toolkit link is now displayed on the Dashboard tab of the new Dynamic List in Plesk Obsidian.
* [*] Improved various interface texts.
* [-] Placeholders like `[at]` used by various plugins no longer trigger false positive alerts during Smart Update procedure. (EXTWPTOOLK-3550)
* [-] Smart Update controls now display proper information about licensing requirements in WordPress Toolkit SE. (EXTWPTOOLK-1462)
* [-] Screenshot separator has been given some growth hormone to make sure it reaches the bottom of the screenshot comparison block at all times. (EXTWPTOOLK-3492)
* [-] Smart Update screenshots were also given growth hormone to make sure they always reach the bottom of the screenshot comparison. (EXTWPTOOLK-3493)
* [-] Smart Update now resets the scroll position between different screens. (EXTWPTOOLK-3475)
* [-] Regular updates won't be accidentally running instead of Smart Updates when Smart Updates are enabled (and expected) on a website. (EXTWPTOOLK-3462)

# 4.3.0 (04 Sep 2019)

* [+] Smart Update feature has been dramatically redesigned, providing full transparency into the analysis process and streamlining overall user experience. Users can now clearly see what is being checked by Smart Updates and what issues are found on which pages. Full analysis summary with update forecast is now also available to users for making an educated decision about the update or for drilling down into issues found by the system.
* [+] Smart Update now analyzes sitemap to determine which pages to check. Users can create a custom sitemap file specifically for Smart Updates to define which pages should be analyzed (up to 30).
* [+] Smart Update will notify users about preexisting issues on the website even if the update process itself went smoothly.
* [+] Smart Update now checks for unexpected PHP errors, warnings, and notices on the website.
* [+] Smart Update now checks for presence of plugin shortcodes, which typically indicates broken plugins.
* [+] WordPress websites using really old PHP versions (5.4 and earlier) are now marked in the WordPress Toolkit UI, displaying a warning that WordPress Toolkit will soon stop supporting such websites. A prompt to change the PHP version is displayed for convenience, if users have the permission to manage PHP version on their website.
* [*] Smart Update toggle is now available as a separate switch on the website card, making sure the feature is easy to see and access.
* [*] Smart Update now gets VIP treatment from the screenshot making service, being finally able to request as many screenshots as needed. 
* [*] Smart Update now detects the database limits before actually trying to clone the website for analysis.
* [*] Smart Update threshold settings were removed as a part of UX streamlining.
* [*] Updates screen was optimized, displaying current and available versions, and also hiding plugin & theme descriptions.
* [*] Smart Update screen displayed upon following the link in the notification email is now branding-neutral.
* [*] The algorithm of making website screenshots for Smart Updates was improved to better reflect the actual website look in certain cases. Finally, users can see the ~~goddamned cactus~~ succulent from the Twenty Seventeen theme in all its glory!
* [-] Smart Update failure no longer has a slim chance to accidentally remove the database of the source website under certain rare circumstances. (EXTWPTOOLK-3312)
* [-] Regular update is no longer stealthily performed instead of Smart Update if WordPress website has enabled password protection. (EXTWPTOOLK-3410)
* [-] Smart Update no longer returns weird error message mentioning website ID if 500 HTTP code is encountered during the Smart Update procedure. (EXTWPTOOLK-3234)
* [-] Smart Update now properly cleans up after itself if the procedure went awry. (EXTWPTOOLK-3313 and EXTWPTOOLK-3424)
* [-] Repeated opening and closing of the Updates window will no longer slow down the system (why would you do that anyway?). (EXTWPTOOLK-2669)
* [-] Improved handling of quantum entanglement in the code now allows WordPress Toolkit to identify more accurately whether a certain WordPress installation is broken or infected at any given moment of time. (EXTWPTOOLK-3330)
* [-] Screenshots can now be made for websites hosted on a domain without `www.` prefix if this prefix is present in the WordPress database as a part of the site URL. (EXTWPTOOLK-2799)
* [-] Smart Update will provide a clear explanation instead of a weird error when a website cannot be updated via Smart Update due to Maintenance Mode being enabled. (EXTWPTOOLK-3264)
* [-] Smart Update will provide a clear explanation instead of a weird error when a website cannot be updated via Smart Update due to password protection being used. (EXTWPTOOLK-3265)
* [-] Smart Update is now correctly handling the situation when someone tries to enable it on a multisite (spoiler: it doesn't work and it never did). (EXTWPTOOLK-3378)
* [-] WordPress installations that were broken and fixed afterwards can now be updated without errors while they're still detected as broken by WordPress Toolkit. (EXTWPTOOLK-3147)
* [-] If some of the items in a batch update were not updated successfully, WordPress Toolkit will now display a proper message, providing the necessary details. (EXTWPTOOLK-3151)
* [-] Sitemap is now properly cloned and copied with all necessary URL replacements during the corresponding procedure. (EXTWPTOOLK-3425)
* [-] WordPress Toolkit now verifies the MD5 checksum of the WordPress core package after downloading it. (EXTWPTOOLK-3270)
* [-] If the original WordPress installation on Apache only hosting had any URL structure enabled in "Permalink settings" (except "Plain"), the installation clone
now works correctly and its links no longer redirect to the original. (EXTWPTOOLK-3484)

# 4.2.2 (08 Aug 2019)

* [*] Integration with Website Overview in Plesk Obsidian was updated, making sure that users can still access WordPress Toolkit quickly on each website.
* [*] `Tools` block was moved to a separate column on the website card for increased visibility and easier access.
* [-] Smart Updates no longer fails to update websites that have issues with infinite redirects. (EXTWPTOOLK-3328)
* [-] IDNs (international domain names) are now properly displayed on the Smart Update comparison screen. (EXTWPTOOLK-3239)
* [-] Website screenshots no longer disappear for reasons unknown when user is opening the Smart Update comparison screen. (EXTWPTOOLK-3260)
* [-] Update of multiple websites should not fail to start anymore in certain cases. (EXTWPTOOLK-3284) 
* [-] WordPress Toolkit now exhibits more patience when connecting remote websites via plugin, ensuring that websites hosted on slower servers can be properly connected without timeouts. (EXTWPTOOLK-3278)

# 4.2.1 (26 Jul 2019)

* [-] Users should now be able to perform Smart Update on websites that have a lot of pages. (EXTWPTOOLK-3283)

# 4.2.0 (25 Jul 2019)

* [+] Users can now upload plugins and themes straight to their website when they open the plugin or theme installation dialog on the website card. 
* [+] Website card now has a link to the corresponding domain in Plesk for easier navigation.
* [*] Smart Update speed was dramatically improved.
* [*] Screenshot comparison screens shown in Smart Update details were streamlined.
* [*] Updates screen was cleaned up and polished, eliminating various small UX issues.
* [*] Website card view was optimized, making the card a bit more compact.
* [*] WordPress Toolkit was finally shamed into regularly cleaning up `wp-cli` utility cache on a per-site basis. 
* [*] The `File Manager` link on the website card is now more visible and prominent.
* [*] WordPress Toolkit now displays more details about the update process of WordPress core, plugins, and themes. This change also affects the Smart Update process, making it more transparent.
* [*] Sites can now be installed and cloned into non-empty directories (including directories with random `.php` files, mummified remains of ancient WordPress sites, and so on). Users will be warned and asked for confirmation if target directory is not empty.
* [*] The task responsible for checking and running automatic updates (`instances-auto-update.php`) was rescheduled to run between 1 AM and 6 AM randomly on each server to avoid causing power surges in datacenters.
* [-] Smart Updates: E-mail notifications about Smart Updates no longer include periods after HTML links (this could break certain links). (EXTWPTOOLK-1759)
* [-] Smart Updates: When users are launching Smart Update while the Smart Update license is expired, a proper message will be displayed in UI. (EXTWPTOOLK-2796)
* [-] Smart Updates: Confusing error message about needing a valid SSL/TLS certificate was unconfused. (EXTWPTOOLK-2599)
* [-] Smart Updates: The system now properly notifies users when Smart Update skips a website for some reason during mass update operation. (EXTWPTOOLK-2733)
* [-] Smart Updates: `Select Page` dropdown now properly displays full website URL of WordPress websites installed in a subdirectory. (EXTWPTOOLK-3224)
* [-] Smart Updates: `Open in Plesk` link no longer overlaps the `Select Page` dropdown in some cases. (EXTWPTOOLK-3203)
* [-] Remote websites with broken database connection are now correctly marked as broken in UI. (EXTWPTOOLK-2950)
* [-] CLI output for remote WordPress websites was made more consistent with the output shown for local WordPress websites. (EXTWPTOOLK-2921) 
* [-] Clicking `Help` in Plesk will now take users to the right help page. (XTWPTOOLK-3091)
* [-] Checking the security status under certain circumstances cannot destroy `Plugins` and `Themes` tabs in website cards anymore. (EXTWPTOOLK-2867)
* [-] Plugins can be added to sets via CLI without the `TypeError` error. (EXTWPTOOLK-3079) 
* [-] When users were choosing to copy only the new database tables using `Copy Data` functionality, all tables were copied instead if one of the new tables didn't have the table prefix. This despicable behavior was nipped in the bud. (EXTWPTOOLK-3123)
* [-] The URL of WordPress website installed on a wildcard subdomain is now displayed correctly. (EXTWPTOOLK-3086)
* [-] `Scan` functionality no longer can be broken by the potential data inconsistency mess left by WordPress websites installed via APS. (EXTWPTOOLK-3065)
* [-] Users cannot start the update process for a website that's already being updated. (EXTWPTOOLK-3174)
* [-] Text placeholders are no longer displayed when looking for certain things in Plesk Search. (EXTWPTOOLK-3004)
* [-] Updating WordPress to a newer version on remote hosting with PHP 5.3 will now show a proper error prompt about PHP requirements. (EXTWPTOOLK-3190)

# 4.1.1 (20 Jun 2019)

* [*] Handling of wp-cli timeouts was improved to avoid putting innocent WordPress sites into quarantine.
* [-] WordPress Toolkit can now connect remote WordPress sites hosted using Bitnami WordPress images from Amazon Marketplace and other cloud marketplaces. (EXTWPTOOLK-3003)
* [-] Successful update of WordPress core from 5.2.1 to 5.2.2 no longer displays an error in WordPress Toolkit UI. (EXTWPTOOLK-3040)
* [-] WordPress Toolkit no longer slows down dramatically when connecting individual remote WordPress sites if their `wp-config.php` has read-only access permission. (EXTWPTOOLK-3007)

# 4.1.0 (30 May 2019)

* [+] You can now connect remote WordPress installations to WordPress Toolkit and manage them without having SSH root access to the remote host. To access this feature, use the `Connect [Beta]` button on the WordPress website list and provide your WordPress administrator credentials. This feature is a part of the overall Remote Management functionality, so it's available only for Server Administrators as a beta feature.
* [+] WordPress websites are now put into quarantine if WordPress Toolkit is not able to properly access certain important files. WordPress Toolkit could not manage such websites previously, since WordPress installation list froze if these websites were encountered. This should also address issues with connecting remote servers with such websites. 
* [*] WordPress Toolkit now provides more information about broken websites to help users identify the website and troubleshoot the problem.
* [*] Remote Management functionality was improved and updated based on the user feedback.
* [*] Clone and Copy Data operations now handle absolute paths in WordPress database. (EXTWPTOOLK-2601)
* [-] Smart Update procedure is now more patient, so it has much less chance to fail because of a timeout. (EXTWPTOOLK-2723)
* [-] Smart Update purchase button is not available to end users anymore. Only server administrators can now purchase or upgrade Smart Update license, as intended. (EXTWPTOOLK-2730) 
* [-] Smart Update procedure steps now communicate better with each other, so issues encountered by one step are now immediately displayed and do not leave the next steps hanging in the dark until the timeout. (EXTWPTOOLK-2734)
* [-] Rollback of security measures that modify `wp-config.php` file won't have a chance of breaking the WordPress website anymore. (EXTWPTOOLK-2824)
* [-] There was a small chance that WordPress website could be accidentally deleted due to inconsistency of WordPress Toolkit database. It would be very painful, so this chance was extinguished. (EXTWPTOOLK-2686)
* [-] Remote Management feature now checks if PHP interpreter on remote server has all required PHP extensions before trying to connect the website. (EXTWPTOOLK-2677)
* [-] Remote Management feature now displays a proper error message if SSH key contents are not valid. (EXTWPTOOLK-2729)
* [-] Customers with multiple subscriptions can now install WordPress on one of them if another subscription does not have the `Database server selection` permission enabled. (EXTWPTOOLK-1940)
* [-] If you were constantly seeing the confusing `Unable to find the task responsible for the currently running update process. Try running the update again.` message when trying to run the updates, you can breathe a sigh of relief now, as we have identified and fixed the root cause of this annoying behavior. (EXTWPTOOLK-2694)
* [-] It's now possible to clone WordPress located in a particular directory to a directory with the same name in a new subdomain. (EXTWPTOOLK-2906)
* [-] Users should no longer see the `Something went wrong` error when trying to select a domain during the cloning. (EXTWPTOOLK-2823)
* [-] WordPress Toolkit no longer tries to activate themes installed through a set. (EXTWPTOOLK-2621)
* [-] Major WordPress autoupdates no longer fail due to timeout. (EXTWPTOOLK-2925)
* [-] Customers won't be seeing the empty `Plugin/theme set` menu during the WordPress installation if the `Allow customers to use sets when they install WordPress` global option is turned off. (EXTWPTOOLK-2692)
* [-] Server Administrators, on the other hand, will be seeing the proper contents of the `Plugin/theme set` menu during the WordPress installation if the `Allow customers to use sets when they install WordPress` global option is turned off. (EXTWPTOOLK-2693)
* [-] Users can now clone WordPress installations located in a subdirectory to the virtual folder root of their subscription. (EXTWPTOOLK-2939)

# 4.0.1 (08 May 2019)

* [-] WordPress Toolkit now displays a correct error message when users are trying to install WordPress 5.2 or update their WordPress to version 5.2 on a domain with PHP version older than PHP 5.6. (EXTWPTOOLK-2902)

# 4.0.0 (25 Mar 2019)

* [+] Beta version of Remote Management functionality is now available. Go to the `Servers` tab and add any Linux-based remote server with WordPress sites to manage them from a single place. This functionality will stay free for a limited time during the Beta stage. A notification will be shown in advance regarding the switch from the free Beta stage to the  Release stage that will require a separate license. Your feedback and input regarding this feature would be highly appreciated.
* [+] Smart Update procedure became more transparent, displaying specific steps and their progress. Now at least you'll know which steps are taking so long!
* [+] Database server info was added to the `Database` tab of the WordPress site card.
* [*] Various links created by WordPress Toolkit on `Websites & Domains` screen are now directing users to the new UI. 
* [*] Users can see the physical path of WordPress sites when cloning them or copying data from one site to another. 
* [*] WordPress Toolkit is now much better prepared both physically and mentally for handling users who try to clone their WordPress site to a destination where another WordPress site already exists.
* [-] Removing a subdomain in Plesk will not remove WordPress installation anymore if this subdomain's docroot was pointing to another domain with WordPress installed. This also covers the use of wildcard subdomains. (EXTWPTOOLK-2580)
* [-] WordPress Toolkit now properly notifies users why Smart Update could not be performed in certain cases. (EXTWPTOOLK-2573)
* [-] The description of `Turn off pingbacks` security measure now explains what will happen if pingbacks are turned off (spoiler: they stop working). (EXTWPTOOLK-2563)
* [-] The em dash punctuation mark is now correctly displayed in plugin and theme names. (EXTWPTOOLK-1990)

# 3.6.3 (06 Mar 2019)

* [-] Cloning procedure now works correctly if `proc_close` or `proc_open` PHP functions are disabled. (EXTWPTOOLK-2533)
* [-] WordPress Toolkit now shows a warning before cloning that `mysqlcheck` utility has detected a database error, so cloning might not work correctly. Users who have not read this warning can continue the cloning procedure. (EXTWPTOOLK-2541)
* [-] The last remnants of upsell prompts for Maintenance Mode were eradicated from the old WordPress Toolkit UI. (EXTWPTOOLK-2540)

# 3.6.2 (26 Feb 2019)

* [*] Maintenance mode management is now available free of charge for owners of Plesk Web Admin edition and similar Plesk editions with basic version of WordPress Toolkit.

# 3.6.1 (23 Feb 2019)

* [-] Maintenance mode no longer gets enabled for no apparent reason after the WordPress Toolkit extension update on websites who have a major WordPress update available. This issue has affected users of basic version of WordPress Toolkit (available in Web Admin and similar editions by default) who have previously enabled the maintenance mode on an affected website at least once. (EXTWPTOOLK-2519)
* [-] WordPress Toolkit database inconsistency no longer has a chance of triggering the removal of certain WordPress websites during the update of WordPress Toolkit extension. (EXTWPTOOLK-2520)

# 3.6.0 (21 Feb 2019)

* [+] Cloning UI was redesigned for improved responsiveness and consistency.
* [+] The UI for copying data (a.k.a. syncing) between installations was redesigned, also for improved responsiveness and consistency. As a side-effect, the procedure formerly known as `Sync` was renamed to `Copy Data`, so users should not be confused about what exactly is going on. 
* [+] Users can now clone WordPress sites to arbitrary subdirectories on target domains.
* [*] Improved the reliability of screenshot generation for WordPress installations, Part II.
* [*] WordPress Toolkit no longer leaves various useless entries in the logs.
* [*] Improved the handling of broken plugins and themes, reducing the number of esoteric error and warning messages shown to users.
* [*] `Install` button now has the focus by default on the WordPress installation form, so hitting Enter after opening the form should immediately launch the installation process.
* [*] Improved the performance of WordPress installation list if it has a lot of WordPress installations. 
* [*] Improved WordPress installation list for viewing on mobile devices.
* [-] WordPress Toolkit database no longer becomes inconsistent when a subscription with two or more WordPress installations is removed. (EXTWPTOOLK-2250)
* [-] Smart Update on Windows servers now checks pages other than the main page. (EXTWPTOOLK-2189)
* [-] Resellers can finally access WordPress Toolkit via the corresponding link in the left navigation panel. (EXTWPTOOLK-1472)
* [-] Users who remove all WordPress installations on the last page in the list of installations are no longer forced to look with despair at the empty screen (unless it was the only page in the list, then yeah). (EXTWPTOOLK-1750)
* [-] `Select All Updates` checkbox on the `Updates` screen is no longer confused about what it should select after several updates were already applied. (EXTWPTOOLK-2175)
* [-] Toolbar buttons above the list of WordPress installations no longer lose their titles after users minimize then maximize the left navigation panel. (EXTWPTOOLK-1394)
* [-] Server Administrator can now manage the `Disable unused scripting` security measure for WordPress installations on locked subscriptions not synchronized with a Service Plan. (EXTWPTOOLK-2178)
* [-] `Disable unused scripting languages` security measure can now be properly applied to WordPress installations on subdomains and additional domains. (EXTWPTOOLK-2323)
* [-] The username and email for WordPress administrator are properly updated in realtime during the WordPress installation procedure if you are changing the destination domain and it has a different owner. (EXTWPTOOLK-2396)
* [-] WordPress Toolkit now properly shows the theme screenshot if it is in the .jpg format (theme screenshots are displayed if WordPress is installed on a domain that does not resolve yet). (EXTWPTOOLK-1907)
* [-] Hotlink Protection And Additional Nginx Directives: `Hotlink Protection` security measure no longer overrides the additional nginx directives on a domain. (EXTWPTOOLK-2305) 
* [-] Hotlink Protection And Mixed Case Domains: `Hotlink Protection` security measure now properly works for domains with mixed case names. (EXTWPTOOLK-2337)
* [-] Hotlink Protection And Expire Headers: `Hotlink Protection` security measure no longer disables Expire headers. (EXTWPTOOLK-2321)
* [-] Update tasks should no longer disappear with cryptic `Unable to find the task responsible for the currently running update process` message. (EXTWPTOOLK-2231)
* [-] WordPress Toolkit now properly cleans up its database when a subdomain with WordPress installation is removed in Plesk. (EXTWPTOOLK-2454)
* [-] `Block access to potentially sensitive files` security measure no longer prevents File Sharing feature in Plesk from working. (EXTWPTOOLK-2279)
* [-] Dramatically reduced the number of false positives for `Block access to potentially sensitive files` security measure. (EXTWPTOOLK-2247)
* [-] Clone procedure now correctly detects and properly modifies certain encoded URLs in the WordPress database. (EXTWPTOOLK-1789)
* [-] Cloned WordPress installations should no longer share their cache with the source installation (we know sharing is caring, but not this time). (EXTWPTOOLK-1773)
* [-] If WordPress Toolkit cannot change the database prefix for all tables when applying the `Database table prefix` security measure, it will properly roll back the changes to prevent website from being broken. (EXTWPTOOLK-2347)
* [-] When WordPress is installed in a subdomain, WordPress Toolkit no longer offers to install it in a subdirectory by default if the main domain already has WordPress installed. (EXTWPTOOLK-2252)
* [-] WordPress can now be installed via CLI into a path containing multiple directories. (EXTWPTOOLK-2260)
* [-] The error message displayed when users try to install WordPress on a domain without an available database now looks nicer. (EXTWPTOOLK-2440)

# 3.5.6 (11 Feb 2019)

* [*] WordPress Toolkit compatibility with Plesk 17.9 Preview releases was improved.
* [-] The limit on WordPress sites with Smart Update in a Service Plan is now correctly applied to each subscription instead of being shared between all subscriptions on this plan. Decommunization is important, comrades. (EXTWPTOOLK-2429)

# 3.5.5 (10 Jan 2019)

* [*] Improved the reliability of screenshot generation for WordPress instances.

# 3.5.4 (25 Dec 2018)

* [-] Listing WordPress instances via CLI now works even if there are inconsistencies in the WordPress Toolkit database. (EXTWPTOOLK-2275)
* [-] Plugin-related PHP warnings no longer prevent WordPress instances from smooth update to version 5.0 on PHP 7.3. (EXTWPTOOLK-2232)
* [-] WordPress can now be installed for those customers who for some mind-boggling reason have no e-mail address specified in Plesk. (EXTWPTOOLK-2274) 
* [-] WordPress Toolkit can now be updated correctly even if there are inconsistencies in its own database. (EXTWPTOOLK-2251)

# 3.5.3 (12 Dec 2018)

* [-] WordPress Toolkit notifications now display proper information again instead of existential emptiness. (EXTWPTOOLK-2220)
* [-] Certain security measures no longer add incorrect directives to the Apache config file if the target WordPress instance contains a space in its path. (EXTWPTOOLK-2210)
* [-] WordPress Toolkit does not stealthily install WordPress in a subdirectory anymore if the target domain already has an `/index.php` file. (EXTWPTOOLK-2208)
* [-] WordPress installation screen no longer takes an obscene amount of time to load if there are a lot of domains on the server. (EXTWPTOOLK-2196)

# 3.5.2 (05 Dec 2018)

* [-] WordPress Toolkit now works properly when Alt-PHP is used as a PHP handler. (EXTWPTOOLK-2192)

# 3.5.1 (03 Dec 2018)

* [-] WordPress sites running in a shared application pool on Windows servers no longer become broken after certain new security measures are applied. (EXTWPTOOLK-2191)

# 3.5.0 (29 Nov 2018)

* [+] A big bunch of new security measures was added to ramp up the security of WordPress instances. The measures are not applied automatically, so all users are shown a notification in UI that prompts them to check and apply the new measures. It's now possible to: 
	* Enable hotlink protection
	* Disable unused scripting languages
	* Disable file editing in WordPress dashboard
	* Enable bot protection
	* Block access to sensitive and potentially sensitive files
	* Block access to `.htaccess` and `.htpasswd`
	* Block author scans
	* Disable PHP executing in various cache folders
* [+] WordPress installation experience was updated to unify the UI, so there are no "quick" and "custom" options anymore. WordPress Toolkit now always displays the installation form with all data prefilled, which allows users to make an informed choice: confirm the defaults to install WordPress quickly, or take your time and change the options you want.
* [+] All users can now choose domains from any accessible subscription when installing WordPress. In practical terms this means that you can now install WordPress anytime you click WordPress in the left navigation panel, even if you're a reseller or server administrator. 
* [+] WordPress Toolkit CLI for installing WordPress instances was updated to include management of automatic update settings. Specifically, the following options were added: `-auto-updates`, `-plugins-auto-updates`, and `-themes-auto-updates`.
* [+] For those who don't want to use Gutenberg yet after WordPress 5.0 is released, we have added a `WordPress Classic` set that includes `Classic Editor` plugin.
* [+] WordPress Toolkit cache can now be cleared with a special CLI command: `plesk ext wp-toolkit --clear-wpt-cache`. This might be useful for handling issues with invalid WordPress Toolkit cache data like corrupted WordPress distributive or broken lists of languages and versions.
* [*] The yellow `Warning` security status was changed to greenish `OK` to avoid scaring innocent users, since it's actually OK to not have every single security measure applied.
* [*] Security measures `Security of wp-content` and `Security of wp-includes` were unnecessarily restrictive, so they were forced to relax their grip somewhat. 
* [-] WordPress Toolkit no longer hangs during the execution of routine daily maintenance tasks when it encounters WordPress instances infected by malware or otherwise operationally challenged. (EXTWPTOOLK-1524)
* [-] Error and warning messages do not display IDN domain names in punycode anymore. (EXTWPTOOLK-1769)
* [-] Resellers and Customers without security management and auto-updates management permissions can no longer manage security and automatic updates. (EXTWPTOOLK-2047)
* [-] WordPress instances no longer become invisible after their installation or cloning process has failed at the very end for some weird reason. (EXTWPTOOLK-1844)
* [-] When users were deleting WordPress instances, WordPress Toolkit was displaying an ambiguous confirmation message, insinuating that WordPress instances will be simply removed from the Toolkit (not deleted). The ambiguity of the message was reduced by several degrees of ambiguousness, so users should now have a very clear idea of what will actually happen. (EXTWPTOOLK-2075)
* [-] `Invalid URL was requested` error is no longer displayed when plugins or themes are activated in the dialog opened directly from the subscription screen. (EXTWPTOOLK-2096)
* [-] WordPress Toolkit no longer refreshes the update cache for detached instances. (EXTWPTOOLK-2049)
* [-] If users are trying to set up Admin credentials for a WordPress instance that does not have any Admin users, WordPress Toolkit does not spectacularly fall on its face anymore, displaying proper error message instead. (EXTWPTOOLK-1826)
* [-] The installation process of WordPress instances is not confused about its own success status anymore if it encounters a file owned by root in the installation directory. (EXTWPTOOLK-2091)
* [-] When WordPress Toolkit encounters a file owned by root during the security status check, it will no longer scare users with a message about the inability to apply a security measure. When the Toolkit finds such a file during the application of security measures, it displays a proper error message now. (EXTWPTOOLK-1875)
* [-] Interface translations no longer display HTML entities in places where they're not supposed to be. (EXTWPTOOLK-2073)
* [-] Removal of multiple instances does not fail anymore if one of the removed instances is broken. (EXTWPTOOLK-1771)
* [-] WordPress Toolkit now properly falls back to the `Install WordPress` service plan option if the `Install WordPress with a set` service plan option was previously selected and this set was removed from the server. (EXTWPTOOLK-1931)
* [-] Smart Update does not enthusiastically notify users about successful updates via notification email anymore if Smart Update was in fact not performed correctly. (EXTWPTOOLK-1760)
* [-] Security status checks became too complacent and stopped working on a routine daily basis. This disgusting behavior was addressed, and users will now be duly notified whenever there's a problem with previously applied security measures. (EXTWPTOOLK-1794)
* [-] Update settings are no longer changed for all WordPress instances selected in the instance list when some of these instances are subsequently filtered out on the Updates screen. (EXTWPTOOLK-2101)
* [-] Smart Update notification emails are now security conscious, providing HTTPS links to Plesk instead of HTTP. (EXTWPTOOLK-1758)
* [-] Cloning procedure now displays proper error message when somebody without the `Subdomain management` permission tries to clone their stuff. (EXTWPTOOLK-1866)
* [-] Failed automatic updates are now properly included in the notification digest. (EXTWPTOOLK-1761)
* [-] WordPress Toolkit has improved its defense against WordPress instances with malformed UTF-8 strings in their settings. Such instances will no longer cause WordPress Toolkit to display a blank screen instead of instance list. (EXTWPTOOLK-1935)
* [-] Users of Russian translation can now see when was the last time WordPress Toolkit checked an instance for updates. (EXTWPTOOLK-1821)
* [-] Speaking of text messages related to updates, a proper error message is now displayed whenever there's a problem with a missing update task. (EXTWPTOOLK-1929)
* [-] WordPress instances that store authentication unique keys and salts in a separate file are no longer considered broken by WordPress Toolkit. (EXTWPTOOLK-2111)
* [-] `Set Contents` pop-up on the WordPress installation screen is now censored out when users open it for a selected set and then switch the set to `None`. (EXTWPTOOLK-1984)
* [-] Maintenance mode no longer displays the countdown on a preview screen if the countdown isn't turned on. Internal debates still rage over whether the Toolkit should play The Final Countdown when it's on, but that's a different story. (EXTWPTOOLK-1845)
* [-] Users will now see a proper error message when they are trying to install WordPress in the same directory where important files like `web.config` were left behind by another WordPress installation. (EXTWPTOOLK-2082)
* [-] WordPress Toolkit now helpfully selects critical security measures not yet applied on the instance when the security scan is ran the first time. (EXTWPTOOLK-2002)
* [-] Text visibility on the Maintenance mode screen was improved to reduce the eye strain of the website visitors around the world. (EXTWPTOOLK-2086)
* [-] Certain placeholder messages were properly localized in the old UI. (EXTWPTOOLK-2021)
* [-] WordPress Toolkit no longer updates the `options` database table of detached WordPress instances when their domain name is changed in Plesk. (EXTWPTOOLK-2074)
* [-] Maintenance mode can now be properly configured if it was never enabled before. (EXTWPTOOLK-2087)
* [-] German translation was updated so that all messages display proper data instead of placeholders. (EXTWPTOOLK-1579)
* [-] `Administrator's username` security measure is not displayed anymore for existing multisite instances, where it doesn't work anyway due to circumstances beyond our control. (EXTWPTOOLK-2106)
* [-] Trying to remove plugins or themes in WordPress Toolkit when they were already removed via other means will now display a proper error message instead of a placeholder. (EXTWPTOOLK-1855)
* [-] Set names are finally restricted to 255 characters, so no more War And Peace on your Sets screen, sorry. (EXTWPTOOLK-1697)
* [-] Maintenance mode screen now properly displays default texts instead of `undefined`. (EXTWPTOOLK-2113)
* [-] Security Status screen can no longer be summoned by users without the corresponding security management permission for a particular instance. Such instances will also no longer be visible on the Security Status screen for multiple instances. (EXTWPTOOLK-1560)
* [-] WordPress Toolkit will display a proper message when one user is trying to secure an instance while another user has already deleted it. (EXTWPTOOLK-1515)
* [-] Redundant requests to wordpress.org on the Plugins and Themes management screens were optimized away. (EXTWPTOOLK-1876)
* [-] The `Select All Updates` checkbox on the Update screen is no longer accessible when users review the intermediate results of the Smart Update procedure. (EXTWPTOOLK-1801)
* [-] The dollar sign displayed on the `Sets` tab when you don't have the full version of WordPress Toolkit is no longer clickable. (EXTWPTOOLK-1822)
* [-] WordPress Toolkit now displays somewhat different result messages when users remove or detach several WordPress instances as opposed to a single one. (EXTWPTOOLK-1755)
* [-] Extremely long WordPress site titles no longer venture outside of the WordPress Toolkit UI. (EXTWPTOOLK-1958)

# 3.4.2 (16 October 2018)

* [*] Improved integration with Advisor extension.

# 3.4.1 (13 September 2018)

* [*] The algorithm used for retrieving the list of plugins and themes was optimized to reduce the load on wordpress.org. 

# 3.4.0 (30 August 2018)

* [+] New CLI commands are now available! You can manage your plugin & theme sets, install them, and upload or remove custom plugins and themes -- all through command line.  Run `plesk ext wp-toolkit --help` to learn more about `sets`, `plugins`, and `themes` commands.
* [+] Security-related screens were redesigned to make them more convenient and usable. In particular, users can now apply any selection of security measures to a number of instances.
* [+] It's now possible to roll back several applied security measures on multiple WordPress instances at once (not that we recommend to do it).
* [+] Users can detach or remove multiple WordPress instances from WordPress Toolkit.
* [+] Server administrators using Plesk versions earlier than Plesk Onyx 17.8 will see a gentle reminder that upgrading their Plesk to version 17.8 or later will give them access to a wonderful world of great new WordPress Toolkit features wrapped in a brand new UI.
* [*] Users can now clearly see when a new website screenshot is being made. Spoilers: the screenshot part of an instance card is temporarily greyed out.
* [*] When you clone WordPress instances, `Search Engine Indexing` is now turned off for the clones by default. Server Administrators can change this behavior on the `Global Settings` tab.
* [*] Screenshots for cloned instances are immediately visible right after the cloning (no more playing hide-and-seek).
* [*] When users synchronize data between WordPress instances, `Files And Databases` option is now selected by default, as opposed to `Files Only` option.
* [*] `Updates` screen for a single WordPress instance now has a magical checkbox that selects or clears all items from `WordPress Core`, `Plugins`, and `Themes` groups.
* [-] Users can now install WordPress instances in subfolders and on additional domains or subdomains even if `wp-config.php` file is present in the parent domain or folder. (EXTWPTOOLK-1765)
* [-] As a corollary of the bugfix mentioned above, users can now clone WordPress instances to additional domains or subdomains even if `wp-config.php` file is present on the parent domain. (EXTWPTOOLK-1766)
* [-] It's now possible to install WordPress into an already existing empty folder. (EXTWPTOOLK-1155)
* [-] Uninstall confirmation dialog in the old UI now has proper text instead of internal localization string. (EXTWPTOOLK-1720)
* [-] WordPress Toolkit no longer redirects users to the first page of the instance list after they have closed the security check screen of an instance located on a different page. (EXTWPTOOLK-1737)
* [-] Custom plugins no longer ignore the `Activate after installation` option, especially if it's not selected. (EXTWPTOOLK-1724)
* [-] WordPress instances with broken database connections can now be found by WordPress Toolkit. Hint: if you fix the database connection, you can manage them in the WordPress Toolkit. (EXTWPTOOLK-1754)
* [-] Smart Updates now work with IDN domains. (EXTWPTOOLK-1719)
* [-] Options on `Update Settings` page will not jump around anymore if you change them before checking for updates has been finished. Note: no options were harmed during the fixing of this bug. (EXTWPTOOLK-1681)
* [-] WordPress Toolkit displays proper error message if one of the instances found during the instance scan is broken. (EXTWPTOOLK-1768)
* [-] CLI command responsible for installing WordPress now adequately explains what's wrong with provided administrator username if there's anything wrong with it. (EXTWPTOOLK-1609)
* [-] WordPress Toolkit no longer executes files of WordPress instances on suspended and disabled domains as a part of its scheduled task. (EXTWPTOOLK-1678)
* [-] Custom themes are now properly activated if `Activate after installation` option is enabled. (EXTWPTOOLK-1717)
* [-] Tooltip is now available for the green icons which indicate that there are no updates on the `Updates` screen shown for multiple instances. (EXTWPTOOLK-1680)
* [-] `wp-config.php` is now removed properly when users remove WordPress instances initially installed as APS packages. (EXTWPTOOLK-1677)
* [-] Smart Update now displays proper error message if it cannot work due to SSL-related problems on the website. (EXTWPTOOLK-1594)
* [-] Security checker `Permissions for files and directories` now should display proper error message if it couldn't do what it had to do. (EXTWPTOOLK-1746)
* [-] `Scan` operation does not refuse to continue working anymore when it encounters a broken instance. (EXTWPTOOLK-1631)

# 3.3.1 (25 July 2018)

* [*] Plugins and themes from the selected set are now properly installed during the provisioning of a subscription with automatic installation of WordPress. (EXTWPTOOLK-1664)  

# 3.3.0 (02 July 2018)

* [+] Filters were added to the plugin and theme installation screen, helping users quickly find what they need (hopefully).
* [+] Users can now check for updates, change update settings and apply updates for multiple WordPress instances at once.
* [+] WordPress Toolkit now has CLI for installing WordPress. Run `plesk ext wp-toolkit --help` for more information.
* [*] Mass security screen is no longer annoying users by constantly rechecking instance security status. You can always recheck the security status by clicking `Check Security` on the Mass Security screen. 
* [-] Security checker `Permissions for files and directories` now agrees that permissions stricter than those set by the checker are not in fact insecure. (EXTWPTOOLK-1577)
* [-] `Log In` button on Websites & Domains screen is no longer displayed on Plesk 17.8 and higher if WordPress access credentials are not known. To make this button appear, go to the WordPress instance list in WordPress Toolkit and specify access credentials for the corresponding instance. Sorry for inconvenience! (EXTWPTOOLK-1573)
* [-] Users can once again change passwords of additional WordPress administrator accounts. (EXTWPTOOLK-1568)
* [-] Server administrators now can manage `Caching (nginx)` checkbox on WordPress instances belonging to subscriptions without the `Manage Hosting` permission. (EXTWPTOOLK-1563)
* [-] This one's somewhat long, so grab your reading glasses. If the administrator username specified during WordPress installation started with a permitted character, but also included forbidden characters, the installation would go on as if nothing wrong happened. However, the administrator username was actually changed during the installation and  the user was not informed about this change, which could be surprising to some users. This behavior was fixed, and username validation works properly now. (EXTWPTOOLK-1561)
* [-] WordPress updates no longer turn off Maintenance Mode if it was enabled before the update. (EXTWPTOOLK-1540)
* [-] Search bars for Plugins and Themes are now separated on Plugin/Theme installation screen. (EXTWPTOOLK-1500)

# 3.2.2 (14 Jun 2018)

* [*] The extension can now be installed on Ubuntu 18.04.

# 3.2.1 (31 May 2018)

* [*] Minor internal security improvements.

# 3.2.0 (24 May 2018)

* [+] New GDPR-compliant interface for installing plugins and themes is now available, completely replacing the old Addendio service. It doesn't have filters yet, but (spoiler alert!) we're working on that.
* [+] Users can now check security and apply critical security fixes for multiple WordPress instances at once. The ability to apply non-critical security fixes en masse was late to the party, so it will have to wait for later WordPress Toolkit releases.
* [*] A couple of new default sets with Jetpack plugin were added.
* [*] `Setup` shortcut was added for those who want to quickly fine-tune their nginx caching settings.
* [*] Smart Update service accuracy was improved. Also, confirmation prompts were added because everybody loves them.
* [-] Toggling stuff like Debug or Maintenance Mode on an instance now immediately updates instance list filters. (EXTWPTOOLK-1389)
* [-] Instance filters went through an extensive bootcamp and became much more useful. You can always see the Filter button now with selected filter and filtered instance count, and you have a "Clear filter" button on the bottom of the instance list as well. (EXTWPTOOLK-1390)
* [-] Smart Update action buttons on the `Updates` screen are now always visible after being taught how to float. (EXTWPTOOLK-1496)
* [-] The "link" button now opens the website in a different tab or window, not in the current one. (EXTWPTOOLK-1445)
* [-] Instance screenshots are now removed if the instance itself is removed (sorry for littering). (EXTWPTOOLK-1413)
* [-] Quick Start menu on the Websites & Domains screen is not hideously deformed on wildcard subdomains anymore. (EXTWPTOOLK-1159)
* [-] If instance cloning has failed during Smart Update, the failed clone is now removed to avoid clone wars (and, uh, copyright infringements). (EXTWPTOOLK-1360)
* [-] Caching management is no longer visible for customers who don't have the permission to manage their hosting settings. (EXTWPTOOLK-1504)
* [-] Users can now turn off countdown timer without having to disable Maintenance mode first. (EXTWPTOOLK-1507)
* [-] In a surprising turn of events, nginx caching management is no longer visible if nginx is not installed on the server. (EXTWPTOOLK-1482)
* [-] Several layout issues were eliminated from the Maintenance mode settings screen. (EXTWPTOOLK-1300)
* [-] It's not possible anymore to confuse Smart Updates by unchecking update items in the middle of Smart Update procedure. (EXTWPTOOLK-1460)

# 3.1.0 (19 April 2018)

* [+] Automatic updates for all plugins or themes on a WordPress instance are now available.
* [+] Smart Update comparison screen was dramatically prettified to the point where it makes certain other screens jealous. The screen also provides more data to help users make informed decisions about whether update will be fine or not.
* [+] Multisite instances are now visually marked in the UI.
* [+] WordPress Toolkit now generates database names with random suffixes when installing WordPress to avoid database name clashes under certain circumstances. Server administrators can also change the database name prefix on the `Global Settings` screen.
* [*] It's now possible to remove multiple plugins or themes at once on the corresponding tabs of an instance.
* [*] Minor improvements and bugfixes related to the new WordPress Toolkit UI.
* [-] Plugins installed on an instance will be visible right away without refreshing the page if all other plugins were previously removed from the instance and the page was not refreshed. (EXTWPTOOLK-1426)
* [-] Smart Update can now be properly performed when `wp-config.php` is located in a non-default folder. (EXTWPTOOLK-1418)
* [-] Preview screenshots now have a much harder time using timeouts to avoid being created. (EXTWPTOOLK-1412)
* [-] Smart Update settings can no longer be tricked into giving the impression of being enabled if the Smart Update is not available for the instance. (EXTWPTOOLK-1379)
* [-] `Updates` screen was trained to be more courageous and can now be successfully opened from the list view. (EXTWPTOOLK-1378)
* [-] `wp-toolkit` CLI utility had some grammar classes and now consistenly understands that `1`, `true`, and `on` all mean one thing (Enabled), while `0`, `false`, and `off` all mean precisely the opposite thing (Disabled). (EXTWPTOOLK-1377)
* [-] Plesk session expiration is now checked on most WordPress Toolkit screens, making for a less confusing working experience. (EXTWPTOOLK-1375)
* [-] Plugins and themes can now be successfully removed in Internet Explorer 11. Why would anyone still use that browser remains a mystery, though. (EXTWPTOOLK-1292)
* [-] Security checker `Permissions for files and directories` now agrees that 750 for directories is quite secure. (EXTWPTOOLK-1103)
* [-] Database naming settings are no longer ignored when WordPress is installed automatically upon the provisioning of a Hosting plan. (EXTWPTOOLK-1098)

# 3.0.5 (11 April 2018)

* [*] Minor improvements and bugfixes related to the new WordPress Toolkit UI.

# 3.0.4 (05 April 2018)

* [*] Improved the reliability of creating instance preview screenshots: WordPress instances were taught to politely stand in the queue instead of overcrowding the screenshotting service like barbarians. (EXTWPTOOLK-1401)
* [-] Activating a theme on a WordPress instance no longer shows themes being switched off on other instances in the list when these instances also have Themes tab opened. (EXTWPTOOLK-1398)

# 3.0.3 (29 March 2018)

* [-] Maintenance screen text is now displayed in English instead of Arabic if WordPress admin UI uses languages not available in Plesk localization packs. (EXTWPTOOLK-1382)
* [-] The contents of the `Actions` dropdown (displayed in the WPT toolbar under certain responsive circumstances) no longer offend the aesthetic sensibilities of users. (EXTWPTOOLK-1355)
* [-] WordPress Toolkit now properly indicates that rollback of an instance restore point has been actually finished. (EXTWPTOOLK-1358) 
* [-] `Scan` and `Import` buttons now work properly when you click on them in the `Actions` dropdown. (EXTWPTOOLK-1362)
* [-] Plesk now properly redirects users to the corresponding page when they remove WordPress instances from `My Apps` screen on the `Applications` tab (ProTip: do not go there for managing your WordPress instances). (EXTWPTOOLK-1365)
* [-] User-provided username will no longer be reset when changing the password in the Password Protection UI. (EXTWPTOOLK-1339)
* [-] Users can now change WordPress admin settings when WPT does not yet know the password to the WordPress instance. (EXTWPTOOLK-1383)
* [-] Smart Update limit in hosting plans is not displayed anymore on Plesk Onyx versions prior to 17.8. (EXTWPTOOLK-1391)

# 3.0.2 (19 March 2018)

* [*] Addendio Plus plugin is no longer installed on all new WordPress instances by default. If you want it to be installed by default, go to WPT Global Settings and enable the corresponding checkbox.
* [-] WPT now properly refreshes instance cache data in Plesk Multi Server environment. (EXTWPTOOLK-1356)
* [-] Users can once again install and manage WordPress instances on domains with PHP 5.3, although we strongly recommend to use at least PHP 5.6 for security reasons. (EXTWPTOOLK-1354)
* [-] Reseller subscriptions can now be customized again without any errors about invalid specified limits. (EXTWPTOOLK-1352)
* [-] Users are now able to remove WordPress instances with missing database. (EXTWPTOOLK-1349)

# 3.0.1 (07 March 2018)

* [*] WordPress Toolkit now properly handles the Plesk session expiration, logging users out and directing them to the login screen whenever the session has expired.
* [-] Smart Update option in Service Plans is now always visible when WordPress Toolkit is installed. (EXTWPTOOLK-1343)
* [-] Database tab is no longer completely broken when it's not possible to fetch all the data that's supposed to be displayed there. (EXTWPTOOLK-1345)
* [-] Document root content will no longer be removed during Smart Update if updated WordPress was installed in a subfolder and no WordPress instance was present in the document root. (EXTWPTOOLK-1344)
* [-] WordPress Toolkit will continue to work nonchalantly if it stumbles upon inconsistencies with WordPress instance restore points. (EXTWPTOOLK-1346)
* [-] It is possible once again to sync data between WordPress instances located on different subscriptions. (EXTWPTOOLK-1348)

# 3.0.0 (06 March 2018)

* [+] Completely redesigned, modern and responsive UI and UX for WordPress instance management. The full list of changes is too numerous to mention here, but the basic idea is: the instance list and overview screen were redesigned and merged into one single UI, providing much better user experience and increased performance. Explore the new WordPress Toolkit and let us know what you think! **Important**: this feature is available only in Plesk Onyx 17.8+.
* [+] Updates can now use the Smart Update service on a per-instance basis. Using Deep Learning algorithms and screenshot analysis, Smart Update checks how the WordPress update would go in a test environment before performing it on the production instance. Glory to our AI Overlords! *ahem* Smart Update supports both automatic and manual updates, providing meatbags with ability to compare the screenshots by themselves. This is a Pro feature that needs to be purchased separately. **Important**: this feature is available only in Plesk Onyx 17.8+.
* [+] Users can enable nginx-based caching via the corresponding switch on the instance card. To configure caching options, go to "Apache & nginx Settings" page on Websites & Domains. **Important**: this feature is available only in Plesk Onyx 17.8+.
* [*] Clone procedure now also watches out for URL changes in certain files. (EXTWPTOOLK-1249)
* [-] Clone procedure no longer fails if `DB_CHARSET` is missing in `wp-config.php` file. (EXTWPTOOLK-1243)
* [-] WordPress Toolkit no longer uses https prefix when automatically installing WordPress during the Service Plan provisioning if SSL/TLS is not available in this Service Plan. (EXTWPTOOLK-1238)
* [-] PHP notices are no longer added to log when you get WordPress instance info from CLI. (EXTWPTOOLK-1308)

# 2.5.2 (21 February 2018)

* [+] The upgrade procedure of the WordPress Toolkit extension was persuaded to be more forgiving -- it can now be successfully repeated if it has previously failed for some reason. (EXTWPTOOLK-1268)
* [-] `Disable scripts concatenation for WP admin panel` security checker no longer invalidates IIS site config if WordPress installation path starts with a digit. (EXTWPTOOLK-1264)

# 2.5.1 (12 February 2018)

* [+] Added new security option that disables script concatenation, preventing certain DoS attacks.

# 2.5.0 (26 December 2017)

* [+] Support for custom plugins and themes. Users can install and manage their own plugins and themes in WordPress through WordPress Toolkit. In addition, server administrators can upload their own plugins and themes to the server-level plugin and theme repositories so that other users on the server can see and install these plugins and themes. Server administrators can also add their plugins and themes to sets for further provisioning.
* [+] Users can install WordPress with a predefined set of plugins and themes during custom WordPress installation. If you do not want your users to access your sets for some reason, you can hide this option on the Global Settings tab.
* [-] The UI hint about WordPress sets preinstallation was not displayed for existing Hosting plans, making it kind of useless. The hint is now displayed for all Hosting plans, regaining its intended usefulness. (EXTWPTOOLK-1081)
* [-] WordPress instance will now be removed from the instance list in WPT if the subscription with this WordPress instance is switched from 'hosting' to 'no hosting'. (EXTWPTOOLK-1043)
* [-] WordPress Toolkit now respects personal boundaries of domains and does not use PHP handler of a parent domain when it should be using PHP handler of the domain where the WordPress is installed. (EXTWPTOOLK-1046)
* [-] Plugin and theme sets are now correctly marked in UI as a feature that requires proper WordPress Toolkit license for users of WordPress Toolkit SE. (EXTWPTOOLK-1039)
* [-] Values of `WP_HOME` and `WP_SITEURL` variables in `wp-config.php` were not properly changed during the cloning of WordPress instances. We've made sure the values of these variables will get proper treatment during the cloning and data synchronization from now on. (EXTWPTOOLK-1069) 
* [-] Maintenance mode assets were not loaded in maintenance mode if any page other than the main page was opened in the browser. (EXTWPTOOLK-978)
* [-] WordPress instances not registered in the WordPress Toolkit were ruthlessly overwritten if somebody performed Quick WordPress installation on the affected domain. WordPress Toolkit was convinced to be more considerate, so now it avoids overwriting unregistered WordPress instances during Quick installation, opting to install new WordPress instances in a subfolder nearby instead. (EXTWPTOOLK-1037)
* [-] PHTML notices are no longer added to `debug.log` on WordPress instance updates. This fix does not affect existing WordPress Toolkit instances which have previously modified Maintenance mode templates, unfortunately. (EXTWPTOOLK-972)
* [-] WordPress Toolkit was displaying a message that a set was installed during the provisioning of a subscription even when nothing of the kind actually happened. This enthusiasm was quite confusing, so WordPress Toolkit now displays the message about set installation only when it is actually installed. (EXTWPTOOLK-1038)
* [-] Instance URLs are now displayed correctly in the Toolkit if `WP_SITEURL` or `WP_HOME` constants in `wp-config.php` have values different from actual website URL. (EXTWPTOOLK-1010)
* [-] The plugin or theme info pop-up window was genetically modified to avoid completely blocking the screen when trying to display a very long plugin or theme name. (EXTWPTOOLK-1012)
* [-] When a WordPress instance without a single plugin was put into maintenance mode, refreshing it in the Toolkit interface resulted in the following error: `Invalid field: slug`. You won't see this error anymore, as all unruly slugs were scurried to graze in the more appropriate fields. (EXTWPTOOLK-1000)

# 2.4.2 (05 December 2017)

* [-] WordPress instances could not be secured via WordPress Toolkit on Plesk 17.8 Preview 8. (EXTWPTOOLK-1004)
* [-] It wasn't possible to install WordPress in the same place three times, overwriting previous installations. We believe that persistence should be rewarded, so we have fixed this issue. (EXTWPTOOLK-1013)

# 2.4.1 (21 November 2017)

* [+] The option to turn off rsync usage for synchronization on Linux was added to Global Settings.
* [-] Addendio service was displaying detached WordPress instances in its drop-down menu. (EXTWPTOOLK-899)
* [-] Successful server backup was adding a warning in the log. (EXTWPTOOLK-991)

# 2.4.0 (16 November 2017)

* [+] Users can specify custom administrator login URL on the "Login Settings" page. This complements various WordPress plugins that change the login URL for security reasons.
* [+] Server Administrator can create sets of themes and plugins for preinstallation with WordPress on new subscriptions.
* [+] On Linux, rsync is now used to synchronize files between instances. This improves performance and adds two more sync options: one allows replacing newer files modified on target (enabled by default), another allows removing files from target that were removed from the source.
* [+] Hosting plans have a new option to preinstall WordPress with an optional predefined set of themes and plugins on newly created subscriptions.
* [+] Multiple WordPress Toolkit settings previously available only via editing `panel.ini` file can now be changed by the server administrator on the Global Settings page of WordPress Toolkit.
* [*] WP-CLI utility was updated to version 1.4.
* [-] WordPress Toolkit could not update secret keys in `wp-config.php` if some of the keys were missing. (EXTWPTOOLK-795)
* [-] Mass update procedure was stopped if a single theme or plugin could not be updated. We have convinced the procedure to continue as usual in this case, and display a warning instead. (EXTWPTOOLK-943)
* [-] Broken WordPress instances registered in WPT could not be repaired by performing data sync from a working instance. (EXTWPTOOLK-904)
* [-] WordPress Drop-Ins were displayed on the "Manage Plugins" page as inactive plugins without descriptions. Attempting to activate them from this page resulted in errors. Now Drop-Ins are not displayed in the plugin list. (EXTWPTOOLK-967)
* [-] When securing database for a WordPress instance, `wp_` substring was replaced not only in the beginning, but also in the middle of table names. (EXTWPTOOLK-905)
* [-] Some operations performed by customers were logged as if they were performed by the server administrator. (EXTWPTOOLK-774)
* [-] On Windows servers it was impossible to clone WordPress instances with files that had spaces in their names. (EXTWPTOOLK-785)
* [-] Under certain circumstances, switching languages took up to several minutes. (EXTWPTOOLK-797)
* [-] After removing a domain that had a subdomain with a WordPress instance registered in WordPress Toolkit, the user could still see this instance in WordPress Toolkit. (EXTWPTOOLK-784)
* [-] Setting `skip_name_resolve = on` in the MySQL server configuration resulted in failure to clone instances. (EXTWPTOOLK-806)
* [-] In some cases WordPress Toolkit did not detect and notify users that a website stopped responding after WordPress instance synchronization. (EXTWPTOOLK-778)
* [-] Addendio service sometimes tried to install Addendio PLUS plugin when it was already installed, which resulted in a warning in the `panel.log` file. (EXTWPTOOLK-913)
* [-] When Resellers used system-wide search, they could see WordPress instances that did not belong to them or their customers. (EXTWPTOOLK-917)

# 2.3.1 (12 October 2017)

* [+] [Addendio](https://addendio.com/) service is now used by default for installing plugins and themes. Enjoy flexible filtering and additional plugin / theme catalogs to choose from.
* [+] When users perform custom WordPress installation, WordPress Toolkit now asks users if they want help with installing plugins.
* [-] After the discussion with WordPress Security team, the 'Version information' security check was removed because it wasn't useful and generated issues in certain cases. (EXTWPTOOLK-852)
* [-] After synchronizing instances, the source instance page had information about the target instance. (EXTWPTOOLK-922)

# 2.3.0 (24 August 2017)

* [+] A restoration point can now be created for a WordPress instance before running operations that have a risk of damaging the instance, such as upgrading it or syncing data. After such operation the instance can be rolled back to the restoration point.
* [+] A new security check 'Disable pingbacks' was added. It prevents attackers from exploiting the WordPress Pingback API to send spam and launch DDoS attacks.
* [+] A link to the list of WordPress instances was added to the left navigation pane in Power User view and the Customer Panel.
* [*] A confirmation dialog is now shown before updating multiple WordPress instances.
* [*] A confirmation dialog is now shown before installing a WordPress instance to a database which is already used by another instance.
* [*] A confirmation dialog is now shown if WordPress installation can overwrite certain files, created by some other CMS.
* [*] Now the WordPress Toolkit does not allow synchronizing databases between WordPress instances that share a single database.
* [-] The message about synchronizing an instance with an older WordPress version to an instance with a newer version was corrected. (EXTWPTOOLK-736)
* [-] The string placeholder was used instead of the domain name on the clone page when German language was used in the user interface. (EXTWPTOOLK-771)
* [-] WordPress Toolkit could not work with instances where the `is_admin` function was used in `wp-config.php`. (EXTWPTOOLK-722)
* [-] Changing the Plesk encryption key after a failed attempt to clone a WordPress instance could result in all further attempts failing. (EXTWPTOOLK-657)
* [-] When cloning a WordPress instance, an error on the database migration step, could result in file transfer step marked as failed. (EXTWPTOOLK-701)
* [-] When cloning an instance, the WordPress Toolkit searched for possible locations of `wp-config.php` in a wrong order, which could result in a failure to clone the instance. (EXTWPTOOLK-704)
* [-] A customer having no access to the WordPress toolkit could indeed have an 'Install Wordpress' button, which actually did not perform any action. (EXTWPTOOLK-721)
* [-] The "Administrator's username" security check was displayed in a wrong section of the Secure WordPress dialog. (EXTWPTOOLK-695)
* [-] Cloning or synchronizing WordPress instances could fail due to unquoted escape sequences in file paths. (EXTWPTOOLK-749)

# 2.2.1 (20 July 2017)

* [-] Some parts of the security check screen didn't show proper text in the Special Edition of the WordPress Toolkit if non-English locale was used. (EXTWPTOOLK-699)
* [-] The buttons on the maintenance mode setup screen had no labels and performed no actions if non-English locale was used. (EXTWPTOOLK-700)

# 2.2.0 (19 July 2017)

* [+] The Special Edition of WordPress Toolkit is now available for all users of Plesk Web Admin edition. This version offers the basic features of WordPress Toolkit for free.
* [*] Improved handling and reporting of WordPress upgrade errors.
* [*] The built-in help for command-line utility has been improved and updated.
* [-] The dialog for removing a broken instance had no text. (EXTWPTOOLK-671)
* [-] After detaching an instance, WordPress Toolkit did not properly set the instance's autoupdate settings. (EXTWPTOOLK-653)
* [-] Spaces were missing in the text on the cloning page for some languages. (EXTWPTOOLK-660)
* [-] When user performed a custom WordPress installation and specified `admin` as a WordPress administrator username, this username was replaced on the Securing Instance step of the installation. Now the `admin` username is not replaced if explicitly specified, and the instance is marked as insecure instead. (EXTWPTOOLK-507)
* [-] During the upgrade, the default WordPress maintenance page was used instead of the maintenance page configured in WordPress Toolkit. (EXTWPTOOLK-644)
* [-] Manually removing a database without using Plesk could result in inability to install or clone WordPress instances. (EXTWPTOOLK-471)
* [-] WordPress Toolkit could not work with an instance that had any code requiring `wp-settings.php` in `wp-config.php`. Now WordPress Toolkit ignores such code when working with the instance and provides improved error reporting for `wp-config.php` issues. (EXTWPTOOLK-638)
* [-] If a theme or a plugin failed to update, no error message was shown. Now WordPress Toolkit shows a comprehensive error message in such case. (EXTWPTOOLK-489)
* [-] Some plugins dependent on other plugins (such as WooCommerce Germanized plugin) could not be activated via the WordPress Toolkit. (EXTWPTOOLK-621)
* [-] Repeating previously failed clone procedure for a WordPress instance failed again if the database user was linked to another database. (EXTWPTOOLK-658)
* [-] Removing the database of a cloned website resulted in inability to clone it again to the same domain and with the same database name. (EXTWPTOOLK-669)
* [-] If user was cloning a subdomain-based WordPress multisite when no valid domains were available, WordPress Toolkit displayed an ugly-looking error without even opening the Clone screen. To avoid hurting the aesthetic sensibilities of users, the error is now displayed properly on the Clone screen and is looking quite fabulous. (EXTWPTOOLK-639)
* [-] If cloning of a WordPress installation was blocked by database import or export errors, the WordPress Toolkit reported that the installation was not configured, but did not explain the actual problem. Now it correctly detects and reports the problem that caused the error. (EXTWPTOOLK-636)
* [-] Themes with descriptions containing non-ASCII characters were breaking the functioning of theme search in WordPress Toolkit. (EXTWPTOOLK-579)
* [-] When synchronizing data between two WordPress instances, the maintenance mode page displayed on the target instance tried to use the resources located on the source instance. (EXTWPTOOLK-631)
* [-] Trying to enable maintenance mode on a WordPress instance of version earlier than 4.3 resulted in an error. (EXTWPTOOLK-686)

# 2.1.2 (29 June 2017)

* [-] Repeatedly scanning a subscription for WordPress instances resulted in autoupdate turned off for all found instances. (EXTWPTOOLK-652)

# 2.1.1 (15 June 2017)

* [-] If the subscription was configured to use PHP 5.3 or earlier, WordPress Toolkit erroneously detected subscription's WordPress instances as broken. (EXTWPTOOLK-632)

# 2.1.0 (14 June 2017)

* [+] Users can now protect their WordPress websites with a password. Anyone browsing a password-protected website receives the "401 Unauthorized" response unless they provide the correct login and password.
* [+] Users can now manually put their WordPress websites into maintenance mode. Users are also able to edit the placeholder page that is displayed to those visiting a WordPress website under maintenance.
* [+] The "WordPress register" event can now be used with Plesk event handlers. The event triggers every time a WordPress website is registered in the WordPress Toolkit after performed scan for WordPress installations or after installation via the Application catalog.
* [*] The WordPress installation procedure was simplified and streamlined.
* [*] The procedure for the installation of WordPress plugins and themes on newly created WordPress websites was simplified and streamlined.
* [-] Under certain circumstances, the administrator's webmail address was displayed incorrectly in WordPress Toolkit. (EXTWPTOOLK-490)
* [-] Importing a WordPress website resulted in an error if no hosting was configured for the parent domain. (EXTWPTOOLK-558)
* [-] In case of available major updates, administrators of WordPress websites with minor automatic updates enabled received daily notifications about installed updates even though these updates were not actually installed. Meanwhile, notifications about available updates were not delivered. (EXTWPTOOLK-561)
* [-] Cloning WordPress websites failed to preserve the source website's automatic update settings. (EXTWPTOOLK-600)

# 2.0.4 (04 May 2017)

* [*] The WP-CLI utility was updated to version 1.1.
* [*] Commands "list" and "info” were added to the WP-CLI utility. WordPress instances can be identified by the combination of "path" and "main-domain-id" (via WP-CLI as well). 
* [*] Titles of WordPress toolkit pages now display WordPress instance URL along with its name. 
* [-] If there were a large number of WordPress instances, during cloning, it took WordPress toolkit a lot of time to generate the list of available domains and subdomains. (EXTWPTOOLK-505)
* [-] There was no warning message that the destination WordPress instance will be replaced by the source one during synchronization. (EXTWPTOOLK-493)
* [-] During synchronization, database tables prefixes were changed even if users selected to synchronize only files. (EXTWPTOOLK-457)
* [-] Error messages were displayed in the panel log after the first WordPress instance installation. (EXTWPTOOLK-454)
* [-] If autoupdate settings were turned on in WordPress toolkit, and later they were changed manually in the configuration file, WordPress toolkit autoupdate settings were not changed accordingly. (EXTWPTOOLK-452) 
* [-] During new APS WordPress installations, the instances were marked as not secure because database tables prefixes were also marked as not secure. (EXTWPTOOLK-395)
* [-] If during WordPress installation the page was refreshed, WordPress installation started again. (EXTWPTOOLK-365)
* [-] If during WordPress installation wordpress.org was not accessible from the Plesk server and the necessary data was not stored in WordPress toolkit cache, Plesk displayed an error message that was not explicit. (EXTWPTOOLK-361)
* [-] WordPress Toolkit was able to generate invalid database table prefixes starting with numbers in exponential notation (for example, 0E70IaqpI). (EXTWPTOOLK-111)
* [-] Context help from all WordPress toolkit screen states did not redirect users to the WordPress related pages in Documentation and Help Portal. (EXTWPTOOLK-6)
* [-] If WordPress Toolkit scanned for new WordPress instances and at least one of new instances was corrupt, scanning was performed with errors and not all new instances were found. (EXTWPTOOLK-477)

# 2.0.3 (13 April 2017)

* [-] A WordPress site could not be cloned if "wp-config.php" file had non UTF-8 encoding. (EXTWPTOOLK-492)
* [-] A WordPress site was cloned incorrectly (some URLs of a clone site referred to the source) if values of "siteurl" and "home" were not the same. (EXTWPTOOLK-488)

# 2.0.2 (30 March 2017)

* [*] A WordPress site installed on a subdomain can now be cloned to a new subdomain of the same domain.
* [-] A WordPress site could not be displayed in browser without manual configuration after cloning to a domain with "Preferred domain" set to a WWW-prefixed URL. (EXTWPTOOLK-474)
* [-] A WordPress site could not be displayed in browser without manual configuration if it was installed on a domain with "Preferred domain" set to a WWW-prefixed URL. (EXTWPTOOLK-472)
* [-] Automatic login to WordPress failed if "Preferred domain" in the domain's hosting settings was set to another URL than the URL of the WordPress instance (for example to a WWW-prefixed URL while the instance had an URL without WWW prefix). (EXTWPTOOLK-470)
* [-] WordPress sites could not be synchronized if proc_open was disabled in PHP settings of the source or destination domain. (EXTWPTOOLK-466)
* [-] A WordPress site could not be cloned if proc_open was disabled in PHP settings of the source or destination domain. (EXTWPTOOLK-456)

# 2.0.1 (27 March 2017)

* [-] A WordPress instance installed via the Application Catalog had a database prefix marked as non-secure. (EXTWPTOOLK-463)
* [-] Automatic login to WordPress failed if the instance was installed using non-secure HTTP and the "Permanent SEO-safe 301 redirect from HTTP to HTTPS" option was enabled in the hosting settings of the domain. (EXTWPTOOLK-462) 
* [-] If an URL of a cloned WordPress instance ended with a slash after registering the instance in WordPress Toolkit, this URL did not change to a new one after cloning. (EXTWPTOOLK-461)
* [-] A page for managing a WordPress instance could not be opened in WordPress Toolkit if the instance used an external MySQL server database not registered in Plesk. (EXTWPTOOLK-460)
* [-] Slashes were present at the end of the URL of a WordPress instance installed via the Applications Catalog. (EXTWPTOOLK-458)
* [-] WordPress could not be installed if proc_open was disabled in a domain's PHP settings. (EXTWPTOOLK-455)

# 2.0.0 (23 March 2017)

* [+] WordPress sites can now be cloned between domains or subscriptions.
* [+] A WordPress site's data (including files and/or database) can be synchronized with another WordPress site.
* [+] A WordPress site can now be imported from another server. The Plesk Migrator extension is required for this functionality.
* [+] Search engine indexing can now be enabled or disabled for a WordPress site.
* [+] The events of creating and removing WordPress instances can now be processed by Plesk.
* [+] It is now possible to enable debugging options for a WordPress site.
* [*] Automatic updates can now be configured to install only the minor (security) updates.
* [*] The WordPress instance management page was improved to display more clear and detailed information.
* [*] The process of WordPress installation is now faster and has more detailed reporting.
* [-] During WordPress installation, WordPress Toolkit did not check if a database with the same name and database user already exists. (EXTWPTOOLK-423)
* [-] During installing WordPress on additional domains in Plesk for Windows, the "write/modify" permissions to the "wp-content" folder were not set automatically. As a result, images and themes of the WordPress installation could not be managed. (EXTWPTOOLK-419)
* [-] When switching to another WordPress instance from a WordPress instance settings dialog, the list of other instances was displayed without URLs. (EXTWPTOOLK-407)
* [-] In some cases, a confusing error message was displayed after WordPress installation was completed. (EXTWPTOOLK-343)
* [-] If MySQL server data directory in Plesk for Windows was changed so that it differed from the location of MySQL server executable files, WordPress could not be installed. (EXTWPTOOLK-326)
* [-] The "wp-config.php" file of a WordPress instance installed via WordPress Toolkit did not contain the "multisite" string, therefore it was inconvenient to enable multi-site WordPress. (EXTWPTOOLK-322)
* [-] When the Keychain for API Secret Keys and WordPress Toolkit extensions were installed in Plesk for Linux, reseller could not log in to Plesk. (EXTWPTOOLK-317)
* [-] Two quick WordPress installations run one by one on a domain, could lead to conflicts.(EXTWPTOOLK-288)
* [-] If an error occurred during WordPress installation, the full error description was not displayed in the maximized progress dialog. (EXTWPTOOLK-286)
* [-] During WordPress installation, the progress dialog was initially displayed minimized without showing information about the installation, and the list of WordPress instances did not refresh after the installation completion. (EXTWPTOOLK-285)
* [-] After renaming a domain with installed WordPress the "Site Address (URL)" parameter in WordPress was not changed. (EXTWPTOOLK-250)
* [-] If the value of the "Preferred domain" parameter was changed for the domain with installed WordPress, the automatic log in to WordPress from the Plesk user interface failed. (EXTWPTOOLK-249)
* [-] When access to WordPress Toolkit was restricted in Plesk configuration, an unclear error message was shown when trying to open WordPress Toolkit. (EXTWPTOOLK-237)
* [-] The "Update" and "View details" links were displayed merged in the Themes and Plugins tabs. (EXTWPTOOLK-141)
* [-] The "Owner" column in the list of WordPress installations contained a broken link if a subscription belonged to the Plesk administrator. (EXTWPTOOLK-33)
* [-] In some cases, WordPress sites were updated automatically even if automatic updates were disabled in their settings. (EXTWPTOOLK-20)
