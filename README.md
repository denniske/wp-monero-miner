# wp-monero-miner

This is the official repository of the WP Monero Miner using Coin Hive wordpress plugin.

You can ask questions here:
https://github.com/denniske/wp-monero-miner/issues


## Description

This plugin enables you to earn money from visitors on your site by using their computing power to mine the cryptocurrency monero.

# Features

Main features:

* **Miner Widget** enabling users on your site to start/stop mining and control mining speed.
* **Background Mining** with configurable CPU usage for mobile and desktop clients
* Login Form PoW ("Proof of Work") **Captchas**
* PoW ("Proof of Work") Verification for **External links**
* **Protected Content Shortcode** for displaying content only when users have mined a specified amount.
* All controls/widgets can be customized visually to fit your page through **Templates**
* Prevention of AdBlock / AV.


Just install this plugin and add the widget "Monero Miner using Coin Hive" to your sidebar. This puts a control panel on your site where each visitor can decide to donate his computing power to you.

To see your earnings you need an account at [https://coinhive.com](https://coinhive.com). There you also find your public site key (public) which you have to put into the settings page of this plugin.

Official plugin website: [http://www.wp-monero-miner.com](http://www.wp-monero-miner.com)

## Installation

Install the plugin and configure it at Settings > WP Monero Miner using Coin Hive.

Then register at [https://coinhive.com](https://coinhive.com). You will then find your public site key (public) at [https://coinhive.com/settings/sites](https://coinhive.com/settings/sites).

Paste this site key at at Settings > WP Monero Miner using Coin Hive.

To start the miner there multiple options. You can place a control panel on your site by using the widget "Monero Miner using Coin Hive" or by placing the shortcode [wp-monero-miner-control] in some page or article. Or you can run in silent mode.

# Miner: Widget

Add the widget "Monero Miner using Coin Hive" to your sidebar. This puts a control panel on your site where each visitor can decide to donate his computing power to you.

If your theme does not support widgets, you can place `<?php echo do_shortcode( '[wp-monero-miner-control]' ); ?>` into the php file of your template.

# Miner: Shortcode

Place the shortcode [wp-monero-miner-control] in some page or article to show a control panel at that position. You can also edit the php files of your theme and use <?php echo do_shortcode( '[wp-monero-miner-control]' ); ?> there to embed the control panel.

# Miner: Silent Mode (Background mining)

Check "silent" checkbox at Settings > WP Monero Miner using Coin Hive. This will start miner when page loaded. No widget needed.

# Protected area (Pro)

Use the following shortcode to create a protected area that only users with more than a specified amount of tokens can see:

`[wp-monero-miner-protected-area tokens=2000000] Secret content. [/wp-monero-miner-protected-area]`

# Host Coin Hive Script (Pro)

Host the scripts from coinhive.com yourself. May prevent blocking by simple adblockers.

# Minify JS/CSS (Basic)

Minify scripts and styles of this plugin for better performance.

# Login Form Captcha

Check "Enable for login" checkbox at Settings > WP Monero Miner using Coin Hive > Captcha. Then PoW captcha from coin hive is displayed at wordpress login form.

# Require PoW for outgoing links

Check "enable" checkbox at Settings > WP Monero Miner using Coin Hive > Links. Then all outgoing links require the user to mine some coins for you before he is redirected to the target page.

## Frequently Asked Questions

# Where can I get a site key / secret key?

Register at [https://coinhive.com](https://coinhive.com). Then get your coin hive public site key (public) and secret key from [https://coinhive.com/settings/sites](https://coinhive.com/settings/sites).

# Where can I see whether miner is running?

Activate 'log' at Settings > WP Monero Miner using Coin Hive. Then open your page and the Chrome Console (F12 > Console). You should see the log output there:

Miner 1.2.0
Miner throttle is 0.5.
Miner autostart is enabled.
Miner cookie is set to 'Mining allowed'.
Miner started.
Miner running with 50 Hashes/s
Miner running with 53 Hashes/s
Miner running with 47 Hashes/s

Remember to disable the 'log' setting again for best performance.

Note: If you have multiple tabs with your page open, the miner will only mine in one tab.

# What are tokens?

If users are logged in on your page and mining they will receive a virtual currency called tokens. A token is a little bit less than a hash. You can use this tokens to give incentive to the user to mine for you.

For example in 'pro' version you can use the following shortcode to create a protected area that only users with more than a specified amount of tokens can see:

`[wp-monero-miner-protected-area tokens=2000000] Secret content. [/wp-monero-miner-protected-area]`

# Where can I see my earnings when pool mining?

See your stats at [http://www.wp-monero-miner.com/pool](http://www.wp-monero-miner.com/pool).

## Screenshots

1. Fill in you site key on the settings page.
2. The sidebar widget in standby.
3. The sidebar widget when mining monero.
4. Log output in chrome console (F12 > Console). (When 'log' settings is activated).

## Changelog

# 2.7.1
* Adapted plugin to wordpress guidelines.

# 2.6.1 - 2.6.3 
* Improved self hosting. (Prevent Adblock/AV)

# 2.6.0 
* (Pro) Added self hosting of coin hive for https://. (Prevent Adblock/AV)
* Improved settings ui with some helper/warning messages

# 2.5.1 - 2.5.3
* Fix: Login Captcha repaired.
* Fix: Redirect link in general.
* Fix: Redirect link templating.
* Pool mining now supports links.

# 2.5.0
* (Pro) Improved self hosting of coin hive.

# 2.4.4
* Fix: Throttle control in miner widget was reset every few minutes.

# 2.4.3
* Fix: Mustache_Autoloader included twice (bug raised by @ui2016)

# 2.4.2
* Throttle control in miner widget saves chosen throttle in cookie.

# 2.4.1
* Fix: Server error

# 2.4.0
* (Pro) Added feature: Templates. (suggested by @marcin11)
* (Standard) Added feature: Throttle control in miner widget. (suggested by @eliot35)
* Added version 'standard'. Please check your version settings at Settings > Standard/Basic/Pro.

# 2.3.1
* Fix: Styling admin miner correctly

# 2.3.0
* (Basic) Only require PoW for listed domains. (suggested by @eliot35)
* Change: Scripts will check whether they are not up to date because they are cached and display warning in chrome console (F12).

# 2.2.1
* Fix: Migrate Throttle/Variant settings properly

# 2.2.0
* (Pro) Protected area shortcode. (suggested by @abdada)
* (Pro) Host Coin Hive Script.
* (Basic) Minify JS/CSS. (suggested by @leopard-lady)
* Change: Introduced min/basic/pro variants. Default is min which has the same features as before the update.
* Change: Throttle is now defined a percentage of cpu power used. Please check if values have been converted properly after update.
* Fix: Mining in admin area although disabled.

# 2.1.1 - 2.1.4
* Fix: Mobile_Detect included twice (bug raised by @dlynch027)
* Fix: Display Hashes/s correctly and fix buttons in widget. (bug raised by @leonvdk)

# 2.1.0
* Added feature: Throttle depending on device type (mobile or not). (suggested by @soft-focus)

# 2.0.0
* Added feature: Translations for miner widget and redirect page. (suggested by @baykanbelirdi)
* Added 'Flush Rewrite Rules' button in Settings > Links
* Added usage data form

# 1.9.1 - 1.9.6
* Using new coinhive.com domain instead of coin-hive.com
* Fix: Total XMR formatting in Settings > Stats
* Fix: Saving of pool settings

# 1.9.0
* Added feature: Pool mining with less minimum payout than coin hive. Useful for small pages.
* Added feature: Toplist widget. (suggested by @leisegang)

# 1.8.1
* Fixed: Again checkboxes in admin settings could not be saved correctly. (bug raised by @soft-focus)

# 1.8.0
* Added feature: Stats in admin backend (site & user toplist). (suggested by @leisegang)

# 1.7.0
* Added feature: Require proof of work for outgoing links.

# 1.6.1
* Fixed: Checkboxes in settings could not be saved correctly. (bug raised by @albirew)

# 1.6.0
* Added feature: Text in widget can be customized. (suggested by @marcin11)

# 1.5.2
* Fixed: Minor bugs fixed.

# 1.5.1
* Fixed: Minor bugs fixed.

# 1.5.0
* Fixed: Miner should now credit mined hashes to wordpress user again. (bug raised by @leisegang)
* Added feature: Proof of Work captcha can be enabled in login form. (suggested by @albirew)

# 1.4.0
* Added feature: Shortcodes. (inspired by @simon1977)
* Added feature: Miner can be run in wordpress admin panel. (suggested by @leisegang)

# 1.3.0
* Added feature: Using current logged in wordpress user for coin hive user list. (suggested by @leisegang)

# 1.2.0
* Added setting 'log'.
* Added feature: When user starts/stops the miner, his decision is stored in a browser cookie. (suggested by @marcin11)
* Listing miner in coin hive user list as "<domain> (wp-monero-miner)"

# 1.1.0
* Added settings 'autostart' and 'silent'.

# 1.0.0
* Initial version.

## Upgrade Notice

# 2.4
Please check your version settings at Settings > Standard/Basic/Pro.

# 2.2.1
Please make sure your `throttle` settings have been migrated to percentage values properly after update.

# 2.2.0
Please make sure your `throttle` settings have been migrated to percentage values properly after update.


## Translations

* English (default)
* German

The plugin can be translated with [Loco Translate](https://de.wordpress.org/plugins/loco-translate).

Send your translations to wpmonerominer@gmail.com and they will be included officially in this plugin.
