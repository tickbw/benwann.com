---
title: WordPress HTML Entities in Posts
author: Ben Wann
type: post
date: 2006-09-29T05:28:17+00:00
url: /2006/09/29/wordpress-html-entities-in-posts/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:26:"http://codex.wordpress.org";s:4:"host";s:19:"codex.wordpress.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:15:"Wordpress Codex";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Craziness

---
Tonight, I was playing around with trying to figure out how to display some HTML entities inside a wordpress post.

I wanted to be able to display a simple fraction in a wordpress post.

After a bit of RTFMing on the [WordPress Codex][1], I found that the tags will allow you to render HTML entities specificly.

The wordpress &#8220;code&#8221; tag will allow you to render specific HTML entities.

Be sure to use the decimal version of the entity rather than the entitized version!!!

Example.

4 `&#188;` x 5 `&#189;`

<!--0fcb5e9076e441907b75194a330c2f73-->

<!--9d456e24cbe3993ee597054c4ebc02ff-->

 [1]: http://codex.wordpress.org