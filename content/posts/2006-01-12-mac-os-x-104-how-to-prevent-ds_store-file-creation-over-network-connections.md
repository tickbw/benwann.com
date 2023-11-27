---
title: 'Mac OS X 10.4: How to prevent .DS_Store file creation over network connections'
author: Ben Wann
type: post
date: 2006-01-12T16:22:34+00:00
url: /2006/01/12/mac-os-x-104-how-to-prevent-ds_store-file-creation-over-network-connections/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count:
  - 1
wpil_links_outbound_internal_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:45:"http://benwann.com/2006/01/12/svn-properties/";s:4:"host";s:11:"benwann.com";s:8:"internal";b:1;s:4:"post";O:15:"Wpil_Model_Post":11:{s:2:"id";i:35;s:5:"title";N;s:4:"type";s:4:"post";s:6:"status";N;s:7:"content";N;s:5:"links";N;s:4:"slug";N;s:6:"clicks";N;s:8:"position";N;s:15:"organic_traffic";N;s:6:"editor";N;}s:6:"anchor";s:9:"this post";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:53:"http://docs.info.apple.com/article.html?artnum=301711";s:4:"host";s:19:"docs.info.apple.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:78:"Mac OS X 10.4: How to prevent .DS_Store file creation over network connections";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - Technology

---
This is really going to be helpful, as I often times need to make photoshop files on my powerbook, but then have to move these files over to a windows machine that is running Apache Tomcat to serve up web applications. .DS_STORE files are the bain of the existence of anybody trying to run a source code repository, as they often time make their way into the repository if people aren&#8217;t watching.

**UPDATE:** Be sure to check out [this post][1] if you dont want .DS_STORE files to ever make it into a subversion source code repository.

NO MORE!!!!!

> [Mac OS X 10.4: How to prevent .DS_Store file creation over network connections][2]  
> This article contains advanced material intended only for those who are looking for information on .DS_Store files. If you do not already have an opinion on this matter, you can disregard this article.
> 
> To configure a Mac OS X user account so that .DS_Store files are not created when interacting with a remote file server using the Finder, follow the steps below.  
> Note: This will affect the user&#8217;s interactions with SMB/CIFS, AFP, NFS, and WebDAV servers.
> 
> 1. Open the Terminal.  
> 2. Type:  
> defaults write com.apple.desktopservices DSDontWriteNetworkStores true  
> 3. Press Return.  
> 4. Restart the computer.
> 
> If you want to prevent .DS_Store file creation for other users on the same computer, log in to each user account and perform the steps aboveâ€”or distribute a copy of your newly modified com.apple.desktopservices.plist file to the ~/Library/Preferences folder of other target users.
> 
> These steps do not prevent the Finder from creating .DS\_Store files on the local volume. These steps do not prevent previously existing .DS\_Store files from being copied to the remote file server. Please note that disabling the creation of .DS_Store files on remote file servers can cause unexpected behavior in the Finder.

<!--214985512e308115a37303909f3b4db9-->

 [1]: https://benwann.com/2006/01/12/svn-properties/
 [2]: http://docs.info.apple.com/article.html?artnum=301711