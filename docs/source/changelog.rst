What's New? - ChangeLog
#######################

openNDS (8.0.0)

  * This version introduces major new functionality and some major changes
  * Rationalisation of support for multiple Linux distributions [bluewavenet]
  * Refactor login.sh script introducing base64 encoding and hashed token (hid) support [bluewavenet]
  * Refactor fas-hid script introducing base64 encoding and simplifying customisation of the script [bluewavenet]
  * Refactor binauth_log.sh and log BinAuth custom data as url encoded [bluewavenet]
  * Refactor fas-aes, simplifying customisation of the script [bluewavenet]
  * Refactor fas-aes-https, simplifying customisation of the script [bluewavenet]
  * Change - Use hid instead of tok when fas_secure_enabled >= 1 [bluewavenet]
  * Add - base64 encoding to fas_secure_enabled level 1 [bluewavenet]
  * Add - gatewyname, clientif, session_start, session_end and last_active to ndsctl json [bluewavenet]
  * Add - support for RFC6585 Status Code 511 - Network Authentication Required [bluewavenet]
  * Add - Client Status Page UI with Logout [bluewavenet]
  * Add - GatewayFQDN option [bluewavenet]
  * Add - client interface to status page query string [bluewavenet]
  * Add - support using base 64 encoded custom string for BinAuth and replace tok with hid [bluewavenet]
  * Add - base 64 decode option to ndsctl [bluewavenet]
  * Add - b64 encoding of querystring for level 1 [bluewavenet]
  * Add - Improved performance/user-experience on congested/slow systems using php FAS scripts [bluewavenet]
  * Add - support for ndsctl auth by hid in client_list [bluewavenet]
  * Add - Ensure faskey is set to default value (always enabled) [bluewavenet]
  * Add - Display error page on login failure in login.sh [bluewavenet]
  * Add - splash.html, add deprecation notice [bluewavenet]
  * Add - authmon, improved lock checking and introduce smaller loopinterval [bluewavenet]
  * Add - client_params, wait for ndsctl if it is busy [bluewavenet]
  * Add - fas-aes-https, allow progressive output to improve user experience on slow links [bluewavenet]
  * Fix - Block access to /opennds_preauth/ if PreAuth not enabled [bluewavenet]
  * Fix - On startup, call iptables_fw_destroy before doing any other setup [bluewavenet]
  * Fix - missing final redirect to originurl in fas-hid [bluewavenet]
  * Fix - ensure gatewayname is always urlencoded [bluewavenet]
  * Fix - client session end not set by binauth [bluewavenet]
  * Fix - Session timeout, if client setting is 0, default to global value [bluewavenet]
  * Fix - missing trailing separator on query and fix some compiler errors [bluewavenet]
  * Fix - ensure authmon daemon is killed if left running from previous crash [bluewavenet]
  * Fix - add missing query separator for custom FAS parameters [bluewavenet]
  * Fix - ndsctl auth, do not set quotas if client is already authenticated [bluewavenet]
  * Fix - client_params, show "Unlimited" when "null" is received from ndsctl json [bluewavenet]
  * Update configuration files [bluewavenet]
  * update documentation [bluewavenet]

 -- Rob White <dot@blue-wave.net> Sat, 2 Jan 2021 16:38:14 +0000

openNDS (7.0.1)

  * This version contains fixes and some minor updates
  * Fix - Failure of Default Dynamic Splash page on some operating systems [bluewavenet]
  * Fix - A compiler warning - some compiler configurations were aborting compilation [bluewavenet]
  * Update - Added helpful comments in configuration files [bluewavenet]
  * Remove - references to deprecated RedirectURL in opennde.conf [bluewavenet]
  * Update - Documentation updates and corrections [bluewavenet]

 -- Rob White <dot@blue-wave.net> Wed, 7 Nov 2020 12:40:33 +0000

openNDS (7.0.0)

  * This version introduces major new enhancements and the disabling or removal of deprecated functionality
  * Fix - get_iface_ip in case of interface is vif or multihomed [bluewavenet]
  * Fix - Add missing client identifier argument in ndsctl help text [bluewavenet]
  * Deprecate - ndsctl clients option [bluewavenet]
  * Add - global quotas to output of ndsctl status [bluewavenet]
  * Fix - fix missing delimiter in fas-hid [bluewavenet]
  * Add - Report Rate Check Window in ndsctl status and show client quotas [bluewavenet]
  * Add - Quota and rate reporting to ndsctl json. Format output and fix json syntax errors [bluewavenet]
  * Fix - get_client_interface for case of iw utility not available [bluewavenet]
  * Fix - php notice for pedantic php servers in post-request [bluewavenet]
  * Add - built in autonomous Walled Garden operation [bluewavenet]
  * Remove - support for deprecated RedirectURL [bluewavenet]
  * Add - gatewaymac to the encrypted query string [bluewavenet]
  * Deprecate - legacy splash.html and disable it [bluewavenet]
  * Add - support for login mode in PreAuth  [bluewavenet]
  * Add - Support for Custom Parameters [bluewavenet]

 -- Rob White <dot@blue-wave.net> Wed, 5 Nov 2020 18:22:32 +0000

openNDS (6.0.0)

  * This version - for Openwrt after 19.07 - for compatibility with new MHD API
  * Set - minimum version of MHD to 0.9.71 for new MHD API [bluewavenet]
  * Set - use_outdated_mhd to 0 (disabled) as default [bluewavenet]
  * Add - Multifield PreAuth login script with css update [bluewavenet]
  * Add - Documentation and config option descriptions for configuring Walled Garden IP Sets

 -- Rob White <dot@blue-wave.net> Wed, 21 Aug 2020 15:43:47 +0000

openNDS (5.2.0)

  * This version - for backport to Openwrt 19.07 - for compatibility with old MHD API
  * Fix - Failure of MHD with some operating systems eg Debian [bluewavenet]
  * Fix - potential buffer truncation in ndsctl
  * Set - use_outdated_mhd to 1 (enabled) as default [bluewavenet]
  * Set - maximum permissible version of MHD to 0.9.70 to ensure old MHD API is used [bluewavenet]

 -- Rob White <dot@blue-wave.net> Wed, 12 Aug 2020 17:43:57 +0000

openNDS (5.1.0)

  * Add - Generic Linux - install opennds.service [bluewavenet]
  * Add - Documentation updates [bluewavenet]
  * Add - config file updates [bluewavenet]
  * Add - Install sitewide username/password splash support files [bluewavenet]
  * Add - quotas to binauth_sitewide [bluewavenet]
  * Add - Splash page updates [bluewavenet]
  * Add - Implement Rate Quotas [bluewavenet]
  * Fix - check if idle preauthenticated [bluewavenet]
  * Add - support for rate quotas [bluewavenet]
  * Fix - Correctly compare client counters and clean up debuglevel messages [bluewavenet]
  * Add - Implement upload/download quotas Update fas-aes-https to support quotas [bluewavenet]
  * Add - Rename demo-preauth scripts and install all scripts [bluewavenet]
  * Add - fas-aes-https layout update [bluewavenet]
  * Add - Set some defaults in fas-aes-https [bluewavenet]
  * Add - custom data string to ndsctl auth [bluewavenet]
  * Add - custom data string to fas-hid.php [bluewavenet]
  * Add - Send custom data field to BinAuth via auth_client method [bluewavenet]
  * Fix - missing token value in auth_client [bluewavenet]
  * Add - upload/download quota and rate configuration values [bluewavenet]
  * Add - Send client token to binauth [bluewavenet]
  * Add - Rename upload_limit and download_limit to upload_rate and download_rate [bluewavenet]
  * Fix - Pass correct session end time to binauth [bluewavenet]
  * Add - some debuglevel 3 messages [bluewavenet]
  * Add - description of the favicon and page footer images [bluewavenet]
  * Add - Authmon collect authentication parameters from fas-aes-https [bluewavenet]
  * Add - sessionlength to ndsctl auth [bluewavenet]
  * Fix - Page fault when ndsctl auth is called and client not found [bluewavenet]
  * Add - Enable BinAuth / fas_secure_enabled level 3 compatibility [bluewavenet]
  * Fix - Correctly set BinAuth session_end [bluewavenet]
  * Add - Updates to Templated Splash pages [bluewavenet]
  * Add - Community Testing files [bluewavenet]
  * Fix - BinAuth error passing client session times [bluewavenet]
  * Fix - PHP notice - undefined constant [bluewavenet]
  * Fix - OpenWrt CONFLICTS variable in Makefile [bluewavenet]

 -- Rob White <dot@blue-wave.net> Wed, 24 Jun 2020 20:55:18 +0000

openNDS (5.0.1)

  * Fix - Path Traversal Attack vulnerability allowed by libmicrohttpd's built in unescape functionality [bluewavenet] [lynxis]

 -- Rob White <dot@blue-wave.net> Wed, 06 May 2020 19:56:27 +0000

openNDS (5.0.0)

  * Import - from NoDogSplash 4.5.0 allowing development without compromising NoDogSplash optimisation for minimum resource utilisation [bluewavenet]
  * Rename - from NoDogSplash to openNDS [bluewavenet]
  * Create - openNDS avatar and splash image [bluewavenet]
  * Move - wait_for_interface to opennds C code ensuring consistent start at boot time for all hardware, OpenWrt and Debian [bluewavenet]
  * Add - Enable https protocol for remote FAS [bluewavenet]
  * Add - trusted devices list to ndsctl json output [bluewavenet]
  * Add - option unescape_callback_enabled [bluewavenet]
  * Add - get_client_token library utility [bluewavenet]
  * Add - utf-8 to PreAuth header [bluewavenet]
  * Add - PreAuth Support for hashed id (hid) if sent by NDS [bluewavenet]
  * Add - library script shebang warning for systems not running Busybox [bluewavenet]
  * Add - htmlentityencode function, encode gatewayname in templated splash page [bluewavenet]
  * Add - htmlentity encode gatewayname on login page (PreAuth) [bluewavenet]
  * Add - Simple customisation of log file location for PreAuth and BinAuth [bluewavenet]
  * Add - option use_outdated_mhd [bluewavenet]
  * Add - url-encode and htmlentity-encode gatewayname on startup [bluewavenet]
  * Add - Allow special characters in username (PreAuth) [bluewavenet]
  * Add - Documentation updates [bluewavenet]
  * Add - Various style and cosmetic updates  [bluewavenet]
  * Fix - Change library script shebang to bash in Debian [bluewavenet]
  * Fix - Remove unnecessary characters causing script execution failure in Debian [bluewavenet]
  * Fix - Add missing NULL parameter in MHD_OPTION_UNESCAPE_CALLBACK [skra72] [bluewavenet]
  * Fix - Script failures running on Openwrt 19.07.0 [bluewavenet]
  * Fix - Preauth, status=authenticated [bluewavenet]
  * Fix - Prevent ndsctl from running if called from a Binauth script. [bluewavenet]
  * Fix - Minor changes in Library scripts for better portability [bluewavenet]
  * Fix - Prevent php notices on pedantic php servers [bluewavenet]
  * Fix - broken remote image retrieval (PreAuth) [bluewavenet]
  * Fix - Allow use of "#" in gatewayname [bluewavenet]

 -- Rob White <dot@blue-wave.net> Sat, 03 Apr 2020 13:23:36 +0000

