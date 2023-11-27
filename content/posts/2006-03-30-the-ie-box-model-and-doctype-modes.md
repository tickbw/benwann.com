---
title: The IE box model and Doctype modes
author: Ben Wann
type: post
date: 2006-03-31T04:10:12+00:00
url: /2006/03/30/the-ie-box-model-and-doctype-modes/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:57:"http://css.maxdesign.com.au/listamatic/about-boxmodel.htm";s:4:"host";s:20:"css.maxdesign.com.au";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:28:"Read the rest of the article";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - Technology

---
This is a great reference on what actually happens on IE in different browsers when working with the IE box model. Great to finally figure out the skinny on how this all fits together. I love this site.

Be sure to read this whole article if you really care to know more about properly rendered HTML.

> **The IE box model and Doctype modes**  
> There are two things you should be aware of when developing CSS styled lists
> 
> 1. IE and the box model  
> 2. IE versions and Doctype modes
> 
> IE and the box model
> 
> Love it or hate it, Internet Explore for Windows is the main browser on the web at present. This means that at some point you will have to deal with IE&#8217;s incorrect interpretation of the box model.
> 
> In simple terms this means that some versions of IE render the box model to a different width than other Standards browsers. So, your CSS styled list may look narrower in IE compared to other browsers.
> 
> The diagram below shows that if a content box is set to 200px wide with 20px of padding and a 20px wide border, the correct method of calculating the overall box width is:  
> content (200px) + padding (20px+20px) + borders (20px+20px) = 280px. 

_[Read the rest of the article][1]_

<!--cfa29c4d9c63b237899c84a738d6720e-->

<!--441e1ddc35333f1bfb51919fbb300d36-->

 [1]: http://css.maxdesign.com.au/listamatic/about-boxmodel.htm