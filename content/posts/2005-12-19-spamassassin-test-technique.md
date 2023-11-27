---
title: SpamAssassin Test Technique
author: Ben Wann
type: post
date: 2005-12-19T16:52:22+00:00
url: /2005/12/19/spamassassin-test-technique/
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
  - Web Hosting

---
SpamAssassin is a great open source software package that provides bayesian spam filtering for email. It is very customizable, and has lots of cool 3rd party plugins for making your life as a server administrator just that much easier.

Lately I was configuring SpamAssassin to do some filtering and needed a way to test that the spam filters were being tripped. Without writing emails that were chock full of obscene words, I found the default text string that triggers an email to be flagged automatically as SPAM. 

> XJS\*C4JDBQADN1.NSBN3\*2IDNEN\*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL\*C.34X

I know this will help some wandering server administrator out there somewhere! 

<!--0e7ea9d6f5036a5758ecc6d70b6b5e0d-->