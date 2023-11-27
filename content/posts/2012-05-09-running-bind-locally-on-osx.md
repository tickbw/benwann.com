---
title: Running BIND locally on OSX
author: Ben Wann
type: post
date: 2012-05-10T04:31:57+00:00
url: /2012/05/09/running-bind-locally-on-osx/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 2
wpil_links_outbound_external_count_data:
  - 'a:2:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:82:"http://intridea.com/posts/using-bind-locally-on-os-x-for-easy-access-to-subdomains";s:4:"host";s:12:"intridea.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"post";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:65:"http://forums.bit-tech.net/showpost.php?p=1599299&amp;postcount=4";s:4:"host";s:19:"forums.bit-tech.net";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"post";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:47+00:00
categories:
  - Craziness

---
Reached the point this evening where I got sick of editing /etc/hosts when doing local development on my MacBookPro.

I have learned enough lately configuring and installing BIND9, that I mustered up the courage to get it running on 127.0.0.1 (theres no place like home).

Using this new fangled Google machine, I drummed up this tasty [post][1].  OSX comes packaged with BIND (named is the daemon name), but it is disabled.  This post gets you setup and running.

The important thing I have to add to this topic, is that I could not for the life of me figure out what I added my local zone file called mysite.local (versus mysite.com for a production BIND DNS server) it would not respond to queries.  Back to the google.

I search for the phrase &#8220;osx bind cant ping local domain&#8221;, and wouldn&#8217;t you know it, the Google machine came through again.  I found this [post][2] dating back from 2002 that solved the problem.  Seeing the date of 2002, I was skeptical since BIND has had some many advances since then, and of course OSX is a totally different beast, but I was desperate.  Low and behold they were correct though.  It appears that Bonjour will snag queries for domains with TLD of &#8220;.local&#8221;, thereby cutting BIND completely out of the deal.

I am sure that there is some configuration that could get one past this, but I am fine just moving my local development domains to .net and calling it a job well done.

Thanks Google machine, what in the world would I do without you! (No seriously, I realized the other day, that I would be 1/100th the programmer I am today, not to mention the productivity and speed, without modern search engines like Google).

 [1]: http://intridea.com/posts/using-bind-locally-on-os-x-for-easy-access-to-subdomains
 [2]: http://forums.bit-tech.net/showpost.php?p=1599299&postcount=4