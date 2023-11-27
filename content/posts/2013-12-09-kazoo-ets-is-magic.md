---
title: Kazoo – ETS is Magic
author: Ben Wann
type: post
date: 2013-12-09T16:21:07+00:00
url: /2013/12/09/kazoo-ets-is-magic/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 2
wpil_links_outbound_external_count_data:
  - 'a:2:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:17:"http://2600hz.com";s:4:"host";s:10:"2600hz.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"Kazoo";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:25:"http://vimeo.com/71320550";s:4:"host";s:9:"vimeo.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:48:"Could not retrieve anchor text, link is embedded";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:47+00:00
categories:
  - Craziness

---
I work on a product called [Kazoo][1].  Kazoo is written in erlang.  Lately at work, those of us on the Platform team have been having a conversation about a language feature known as ETS (erlang term storage). The end of the conversation pretty much always concludes that

> Erlang ETS == Magical

I have been down the road of finding a magical language feature (not in erlang) for a specific use case, only later to find out that when I switch the conditions of the use case, it totally and completely falls apart.  With that in mind, this weekend I did a little reading / researching / googling to find the source of the magic.

Thanks for Erlang Solutions for posting the Videos from the latest Erlang Factory in Sweden, had a talk specifically about benchmarking ETS.  This was really awesome, and anyone who cares about ETS should watch it.

> tl;dw &#8211; ETS is MAGIC, however, if you are trying to scale a product using ETS, be VERY aware of the number of physical chips on the server vs. the number of cores on those chips.  There are runtime flags to pin process schedulers to individual cores, but there are tradeoffs.
> 
> [<img decoding="async" loading="lazy" class="size-medium wp-image-1101 alignleft" alt="Screen Shot 2013-12-09 at 10.19.30 AM" src="https://benwann.com/wp-content/uploads/2013/12/Screen-Shot-2013-12-09-at-10.19.30-AM-300x143.png" width="300" height="143" srcset="https://benwann.com/wp-content/uploads/2013/12/Screen-Shot-2013-12-09-at-10.19.30-AM-300x143.png 300w, https://benwann.com/wp-content/uploads/2013/12/Screen-Shot-2013-12-09-at-10.19.30-AM.png 1005w" sizes="(max-width: 300px) 100vw, 300px" />][2]

&nbsp;

&nbsp;

&nbsp;



&nbsp;

 [1]: http://2600hz.com
 [2]: https://benwann.com/wp-content/uploads/2013/12/Screen-Shot-2013-12-09-at-10.19.30-AM.png