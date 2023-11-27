---
title: Mercurial Add All Unversioned File
author: Ben Wann
type: post
date: 2012-05-10T04:21:23+00:00
url: /2012/05/09/mercurial-add-all-unversioned-file/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count_data:
  - 'a:0:{}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:47+00:00
categories:
  - Craziness

---
Needed to add a bunch of files to my (mercurial) hg repo and realized that a command I use all the time in subversion (svn) repos.

> hg st | grep ? | sed &#8216;s/? *//&#8217; | xargs hg add

Break it down for ya.  Remember the &#8220;|&#8221; unix character takes the results of stdout and pipes that as the inputs to the next chain in the command.  For the purposes of explanation, assume I were to create a file called testfile.js in the &#8220;js&#8221; directory in my repo directory.

1. hg st &#8211; this displays the files in an hg repo that are currently not versioned in the repo.  Results are sent to stdout.

Results:

? js/testfile.js

2. grep ? &#8211; This looks at each line and returns it valid if there is a ? in the string.

Results:

? js/testfile.js

3. sed &#8216;s/? *//&#8217; &#8211; sed is an awesome text tool for performing operations on text,  in this case a executing a regex on each line that removes that ? from the text.  This is important because the next command does not recognize &#8220;?&#8221; as in the filename.

Results:

js/testfile.js

4. xargs hg add &#8211; Finally, we execute the command on the sanitized string.

A js/testfile.js

Enjoy!