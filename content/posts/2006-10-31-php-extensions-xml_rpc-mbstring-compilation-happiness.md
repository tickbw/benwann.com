---
title: PHP Extensions XML_RPC + mbstring != Compilation Happiness
author: Ben Wann
type: post
date: 2006-10-31T07:54:59+00:00
url: /2006/10/31/php-extensions-xml_rpc-mbstring-compilation-happiness/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:36:"http://bugs.php.net/bug.php?id=34221";s:4:"host";s:12:"bugs.php.net";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"link";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Craziness
  - Mac OSX
  - Nerd
  - PHP
  - Technology

---
If the title of this blog post doesn&#8217;t explain it enough here it is.

This evening, well early morning, I was trying to get XML_RPC to install as the native extension.Â  I had previously install PHP 5.1.6 with the mbstring extension enabled to make a pesky phpMyAdmin error about it go away.

Well this time it caught up with me.Â  I tries to compile PHP with the same previous settings, now adding XML_RPC.Â  Well thank heavens for the bug tracking system at PHP, I found out why I failed.

Here is the [link][1] to why it failed.

Hope this can help someone out there! Until next time, happy coding, and remember, always practice safe hex.</p> 

<!--7f228d0c4766da0ce2061db27f9e98c4-->

<!--0fd0bc0ceaba653f80edd0174924a30f-->

 [1]: http://bugs.php.net/bug.php?id=34221