---
title: Stray Notes Â» Blog Archive Â» Running Kcachegrind on Mac OSX 10.4
author: Ben Wann
type: post
date: 2006-10-26T17:49:13+00:00
url: /2006/10/26/stray-notes-»-blog-archive-»-running-kcachegrind-on-mac-osx-104/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count:
  - 1
wpil_links_outbound_internal_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:54:"http://benwann.com/2006/10/06/getting-rich-with-php-5/";s:4:"host";s:11:"benwann.com";s:8:"internal";b:1;s:4:"post";O:15:"Wpil_Model_Post":11:{s:2:"id";i:73;s:5:"title";N;s:4:"type";s:4:"post";s:6:"status";N;s:7:"content";N;s:5:"links";N;s:4:"slug";N;s:6:"clicks";N;s:8:"position";N;s:15:"organic_traffic";N;s:6:"editor";N;}s:6:"anchor";s:18:"Get Rich with PHP5";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_links_outbound_external_count:
  - 2
wpil_links_outbound_external_count_data:
  - 'a:2:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:39:"http://www.acme.com/software/http_load/";s:4:"host";s:8:"acme.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"here";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:32:"http://brent.izolo.com/blog/?p=4";s:4:"host";s:15:"brent.izolo.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:70:"Stray Notes Â» Blog Archive Â» Running Kcachegrind on Mac OSX 10.4";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - How-To
  - Mac OSX
  - Nerd
  - PHP
  - rants
  - Technology

---
I posted earlier on how to [Get Rich with PHP5][1].

In that article Rasmus Lerdorf writes about how to use a certain set of debugging tools as well as PECL packages and database modifications to really tweak some serious speed out of your PHP web application.

I use a powerbook G4 for my PHP hackery, so some of the tools he mentioned are not available with a deault OSX 10.4 installation.Â  So I thought, hey lets write a how to install to make this work!!

First lets get a little tool called http_load. Get it [here][2].

Untar the file.

> tar zxvf http_load-12mar2006.tar.gz

run make

I recommend copying http_load to a directory like /usr/local/bin or /usr/local/sbin &#8230; basically somewhere in your path 🙂

Now lets install kcachegrind.Â  For that, follow this link over to the stray notes blog.

[Stray Notes Â» Blog Archive Â» Running Kcachegrind on Mac OSX 10.4][3]  
Running Kcachegrind on Mac OSX 10.4

Now with both of those installed, you should be ready to go!

Debug your hearts out people! 

<!--d198deec426439e7a08c9a9b931cbac5-->

 [1]: https://benwann.com/2006/10/06/getting-rich-with-php-5/
 [2]: http://www.acme.com/software/http_load/
 [3]: http://brent.izolo.com/blog/?p=4