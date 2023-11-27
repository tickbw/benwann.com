---
title: G4 Freeze Your Computer Needs to be Restarted
author: Ben Wann
type: post
date: 2006-03-03T17:46:42+00:00
url: /2006/03/03/g4-freeze-your-computer-needs-to-be-restarted/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 1
wpil_links_outbound_external_count_data:
  - 'a:1:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:100:"http://www.macosx.com/content/faq.php/q6252/Emac-G4-Freeze--your-Computer-Needs-to-Be-Restarted.html";s:4:"host";s:10:"macosx.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:54:"Thanks to Tech Support Technician "bobw" at Macosx.com";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - St.Louis
  - Technology

---
Was having all sorts of problems with my G4 17&#8243; Powerbook today and last night, thought I would give this a try.

[Thanks to Tech Support Technician &#8220;bobw&#8221; at Macosx.com][1]

>   * First disconnect anything connected to the machine (printer,modem, scanner, etc) and see if the Kernel panic still happen. (&#8216;your computer needs to be restarted&#8217; in various different languages is a Kernel panic)
>   * Next, run Disk Utility from your Utility folder to Repair Permissions.
>   * Next run &#8216;fsck&#8217;;
> 
> To run fsck, you first need to start up your Mac in single-user mode. Here&#8217;s how:
> 
>   1. Restart your Mac.
>   2. Immediately press and hold the Command and &#8220;S&#8221; keys.
> 
> You&#8217;ll see a bunch of text begin scrolling on your screen. In a few more seconds, you&#8217;ll see the Unix command line prompt (#).
> 
> You&#8217;re now in single-user mode.
> 
> Now that you&#8217;re at the # prompt, here&#8217;s how to run fsck:
> 
>   1. Type: &#8220;fsck -f&#8221; (that&#8217;s fsck-space-minus-f).
>   2. Press Return.
> The fsck utility will blast some text onto your screen. If there&#8217;s damage to your disk, you&#8217;ll see a message that says:
> 
> **\*\\*\* FILE SYSTEM WAS MODIFIED \*\*\***
> 
> If you see this message&#8211;and this is extremely important&#8211; repeat running fsck. It is normal to have to run fsck more than once &#8212; the first run&#8217;s repairs often uncover additional problems..
> 
> When fsck finally reports that no problems were found, and the # prompt reappears:
> 
>   3. Type: &#8220;reboot&#8221; to restart, or type &#8220;exit&#8221; to start up without rebooting.
>   4. Press Return.
> Your Mac should proceed to start up normally to the login window or the Finder. 

<!--aa9ebdc1095b073ae92009203a0dfeec-->

 [1]: http://www.macosx.com/content/faq.php/q6252/Emac-G4-Freeze--your-Computer-Needs-to-Be-Restarted.html