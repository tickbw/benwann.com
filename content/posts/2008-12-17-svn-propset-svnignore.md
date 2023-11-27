---
title: SVN PROPSET SVN:IGNORE
author: Ben Wann
type: post
date: 2008-12-17T15:41:13+00:00
url: /2008/12/17/svn-propset-svnignore/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count_data:
  - 'a:0:{}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - Technology

---
Here is a helpful Subversion Command to set the svn keyword svn:ignore on all of the directories from a certain location.

> <pre class="code">svn propset svn:ignore '*' .</pre>

This has proven very helpful in situations where I have a web site that has a directory structure that is dynamic to the web application.

I do not want all of those files in version control as they are not the same from one deployment to the next.Â  They also typically match the database entries, which vary from one deployment to another.

Enjoy!

>