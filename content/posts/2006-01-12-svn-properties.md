---
title: Subversion Properties – SVN:ignore
author: Ben Wann
type: post
date: 2006-01-12T16:29:40+00:00
url: /2006/01/12/svn-properties/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:46:"https://benwann.com/2006/01/12/svn-properties/";s:4:"host";s:11:"benwann.com";s:8:"internal";b:1;s:4:"post";O:15:"Wpil_Model_Post":11:{s:2:"id";i:34;s:5:"title";N;s:4:"type";s:4:"post";s:6:"status";N;s:7:"content";N;s:5:"links";N;s:4:"slug";N;s:6:"clicks";N;s:8:"position";N;s:15:"organic_traffic";N;s:6:"editor";N;}s:6:"anchor";s:9:"this post";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 2
wpil_links_outbound_external_count_data:
  - 'a:2:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:47:"http://svnbook.red-bean.com/en/1.1/ch07s02.html";s:4:"host";s:20:"svnbook.red-bean.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:14:"SVN Properties";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:64:"http://svnbook.red-bean.com/en/1.1/ch07.html#svn-ch-7-sect-1.3.2";s:4:"host";s:20:"svnbook.red-bean.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:36:"see the section called â€œConfig";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - Technology

---
This will actually help to not let .DS_STORE files into a Subversion source code repository.  
Protect yourself, beforeyou wreck yourself I say! (Note taken from the early english saying &#8220;Check yoself, befo you wreck yoself!&#8221;)

> [SVN Properties][1]  
> svn:ignore
> 
> The svn:ignore property contains a list of file patterns which certain Subversion operations will ignore. Perhaps the most commonly used special property, it works in conjunction with the global-ignores run-time configuration option ([see the section called â€œConfig][2]â€) to filter unversioned files and directories out of commands svn status, svn add, and svn import.
> 
> The rationale behind the svn:ignore property is easily explained. Subversion does not assume that every file or subdirectory in a working copy directory is intended for version control. Resources must be explicitly placed under Subversion&#8217;s management using the svn add or svn import commands. As a result, there are often many resources in a working copy that are not versioned.

<!--f7db6ae35921448a465f4bfb8227cb77-->

 [1]: http://svnbook.red-bean.com/en/1.1/ch07s02.html
 [2]: http://svnbook.red-bean.com/en/1.1/ch07.html#svn-ch-7-sect-1.3.2