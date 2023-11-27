---
title: IE innerHTML on Table Element
author: Ben Wann
type: post
date: 2007-01-16T13:41:26+00:00
url: /2007/01/16/ie-innerhtml-on-table-element/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 12
wpil_links_outbound_external_count_data:
  - 'a:12:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:73:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/col.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:3:"COL";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:78:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/colgroup.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:8:"COLGROUP";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:2;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:78:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/frameset.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:8:"FRAMESET";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:3;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:74:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/html.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"HTML";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:4;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:75:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/style.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"STYLE";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:5;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:75:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/table.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"TABLE";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:6;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:75:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/tbody.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"TBODY";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:7;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:75:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/tfoot.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"TFOOT";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:8;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:75:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/thead.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"THEAD";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:9;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:75:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/title.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:5:"TITLE";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:10;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:72:"http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/tr.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:2:"TR";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:11;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:82:"http://msdn.microsoft.com/workshop/author/dhtml/reference/properties/innerhtml.asp";s:4:"host";s:18:"msdn.microsoft.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:82:"http://msdn.microsoft.com/workshop/author/dhtml/reference/properties/innerhtml.asp";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Craziness

---
Spent a bit of yesterday figuring out why I couldn&#8217;t set an innerHTML on a HTML Table Element.

Come to find out that IE has the innerHTML element set to read-only for the following elements:

[COL][1], [COLGROUP][2], [FRAMESET][3], [HTML][4], [STYLE][5], [TABLE][6], [TBODY][7], [TFOOT][8], [THEAD][9], [TITLE][10], [TR][11].  
You can read the exact specs for the IE innerHTML property here:

<http://msdn.microsoft.com/workshop/author/dhtml/reference/properties/innerhtml.asp></p> 

<!--076af80cb8a810579102e347c9ef1d26-->

<!--28a0490b372cd2a0e05fd85df1e6a320-->

 [1]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/col.asp
 [2]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/colgroup.asp
 [3]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/frameset.asp
 [4]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/html.asp
 [5]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/style.asp
 [6]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/table.asp
 [7]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/tbody.asp
 [8]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/tfoot.asp
 [9]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/thead.asp
 [10]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/title.asp
 [11]: http://msdn.microsoft.com/workshop/author/dhtml/reference/objects/tr.asp