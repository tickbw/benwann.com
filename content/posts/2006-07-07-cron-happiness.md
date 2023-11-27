---
title: Cron Happiness
author: Ben Wann
type: post
date: 2006-07-07T16:47:41+00:00
url: /2006/07/07/cron-happiness/
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
  - Craziness

---
Today, I spent time digging through the crontab file on a server out on the internets.

Wondering why all of sudden the cron jobs I set up stopped working.

If anyone was wondering how to mail yourself if the *nix user your cron job is running under is not where you check you email, then hopefully this post can give you a hand.

Your cron job should look like this

30 12 \* \* \* \* &#8220;command to use&#8221; &#8220;full path to script&#8221;

That would execute the script everyday at 12:30 (Server Time &#8230; Dont forget those Time Zones all you remote admins!!!).  
Once script execution is done, it will then email the results of the script to the user executing. Somewhere outthere in wonderland, if the script outputs anything to stdout, it would show up on the screen, and then email those results to the user.

If you want to also email the results to an address not on the machine, then do the following:

30 12 \* \* \* \* &#8220;command to use&#8221; &#8220;full path to script&#8221; | mail -s &#8220;Test&#8221; no@no.com

This would use the *nix pipe command to push the results of script execution in an email to &#8220;no@no.com&#8221; with &#8220;Test&#8221; as a subject.

Hope this helps!!! 

<!--849d915d096f53966987ceb2b465ecd3-->