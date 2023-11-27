---
title: 'Text* Snippets: Recursively remove all .svn directories [shell] [svn] [bash]'
author: Ben Wann
type: post
date: 2007-10-18T20:33:47+00:00
url: /2007/10/18/text-snippets-recursively-remove-all-svn-directories-shell-svn-bash/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:38:"http://textsnippets.com/posts/show/104";s:4:"host";s:16:"textsnippets.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:76:"Text* Snippets: Recursively remove all .svn directories [shell] [svn] [bash]";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - How-To
  - Nerd
  - Technology

---
<a target="_blank" href="http://textsnippets.com/posts/show/104">Text* Snippets: Recursively remove all .svn directories [shell] [svn] [bash]</a>

I am always looking for this command.

Usually, you if you need a code base without the .svn directories, you can just do an svn export. This is especially good for deploying to web applications from known revisions/releases inside of version control.

Sometimes however, there arises the situation where a collection of files that were once in version control, and were orphaned for whatever reason, and that code needs to get re-added to version control, the .svn directories present in the directories will conflict with a new svn add command. In that case use this command:

<pre><span class="ident">find</span> <span class="punct">.</span> <span class="punct">-</span><span class="ident">name</span> <span class="punct">.</span><span class="ident">svn</span> <span class="punct">-</span><span class="ident">print0</span> <span class="punct">|</span> <span class="ident">xargs</span> <span class="punct">-</span><span class="number"></span> <span class="ident">rm</span> <span class="punct">-</span><span class="ident">rf</span></pre>

<pre></pre>

<p style="margin-left: 40px">
  <!--2b02b1dbdabe5a7297acf208f87d49a4-->
</p>

<!--e2e1b33abd820355616ad1ff02a03ac3-->

<!--23fbf1291741d991925474dbe2cae500-->