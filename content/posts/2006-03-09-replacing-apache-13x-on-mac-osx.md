---
title: Replacing Apache 1.3.x with 2.0.x on Mac OSX
author: Ben Wann
type: post
date: 2006-03-10T00:05:59+00:00
url: /2006/03/09/replacing-apache-13x-on-mac-osx/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 2
wpil_links_outbound_external_count_data:
  - |
    a:2:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:30:"http://www.itstud.chalmers.se/";s:4:"host";s:18:"itstud.chalmers.se";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:28:"Chalmers Tekniska Hogskola's";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:46:"http://www.itstud.chalmers.se/~it2bjar/macosx/";s:4:"host";s:18:"itstud.chalmers.se";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:32:"Installing Apache2 and PHP 5.0.4";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - Serafini Studios
  - Technology

---
I found a great HOW-TO on how to replace the base installation of Apache 1.3.x on Mac OSX over at [Chalmers Tekniska Hogskola&#8217;s][1] website.

This is very helpful information if you use apache on your Mac to develop websites and web applications locally.

Without further ado, here is the article.

> [Installing Apache2 and PHP 5.0.4][2]
> 
> Staying at the top has a cost. Hours of trying to figure out how to install new software.  
> Recently I (after lots of mistakes) managed to install Apache2 and PHP 5.0.4. To make it all simple for and only invent the wheel once I decided to put up this guide.  
> The idea was that I wanted Apache2 together with PHP on my webserver and start and stop Apache from the System Preferences pane. In other words I wanted to remove the old installation of Apache 1.3.x and replace it with Apache2. Roaming the Internet gave me absoulutly no clue whats so ever how to achive this. The guides I found was generally set up so you had two webservers or a lot of fiddling with the httpd.conf file. Also I would have to make a script to launch Apache2 at startup, and as said before &#8220;There is no reason to invent the wheel again&#8221;.  
> So here is what you need to do: I assume that you are familiar with using a terminal window, if not, this is a good time to try it out.  
> Prerequisites:  
> You need to have a compiler installed. This comes for free with XCode. I&#8217;m running gcc 4.0.  
> glibtool (GNU Libtool) version 1.4.2 or higher  
> autoconf verion 2.5.2 If you don&#8217;t have these download them using fink. If you don&#8217;t have fink, download and install it! These are needed for the installation of Apache2 . If you don&#8217;t want to use fink Remember that GNU Libtool is in a normal *unix system named libtool. If you don&#8217;t compile it as glibtool you will run into trouble later on when installing other programs developed by Apple. 

<!--f45d410262779af6f89464a77c8337d6-->

 [1]: http://www.itstud.chalmers.se/
 [2]: http://www.itstud.chalmers.se/~it2bjar/macosx/