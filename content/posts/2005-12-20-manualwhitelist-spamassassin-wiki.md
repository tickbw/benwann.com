---
title: ManualWhitelist – Spamassassin Wiki
author: Ben Wann
type: post
date: 2005-12-20T17:36:07+00:00
url: /2005/12/20/manualwhitelist-spamassassin-wiki/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:51:"http://wiki.apache.org/spamassassin/ManualWhitelist";s:4:"host";s:15:"wiki.apache.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:35:"ManualWhitelist - Spamassassin Wiki";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Technology
  - Web Hosting

---
The Spamassassin chronicles continue, now I know how to manually whitelist a single user or an entire domain of users. See below for the technique.

> [ManualWhitelist &#8211; Spamassassin Wiki][1]  
> ManualWhitelist  
> Whitelisting a user
> 
> Adding a user to your whitelist gives them a -100 score, which has the effect of always marking their mail as non-spam.
> 
> To manually whitelist a particular address, say d.cary@sparkingwire.com, edit your local user prefs file ~/.spamassassin/user_prefs:
> 
> \# whitelist David Cary:  
> whitelist_from d.cary@sparkingwire.com
> 
> Whitelist and blacklist addresses are file-glob-style patterns, so friend@somewhere.com, \*@isp.com, or \*.domain.net will all work.
> 
> \# whitelist everyone at sparkingwire.com:  
> whitelist_from *@sparkingwire.com

<!--dea9c888d15204f3c9889443e249de4a-->

 [1]: http://wiki.apache.org/spamassassin/ManualWhitelist