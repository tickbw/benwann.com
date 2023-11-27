---
title: PHP 5.2.6 on OSX Tiger 10.4.11 Compiled with FreeTDS
author: Ben Wann
type: post
date: 2008-09-24T15:19:55+00:00
url: /2008/09/24/php-526-on-osx-tiger-10411-compiled-with-freetds/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 10
wpil_links_outbound_external_count_data:
  - 'a:10:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:20:"http://jwebmedia.com";s:4:"host";s:13:"jwebmedia.com";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"jWeb";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:18:"http://freetds.org";s:4:"host";s:11:"freetds.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:7:"FreeTDS";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:2;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:71:"ftp://ftp.ibiblio.org/pub/Linux/ALPHA/freetds/stable/freetds-stable.tgz";s:4:"host";s:15:"ftp.ibiblio.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"here";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:3;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:71:"ftp://ftp.ibiblio.org/pub/Linux/ALPHA/freetds/stable/freetds-stable.tgz";s:4:"host";s:15:"ftp.ibiblio.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:48:"Could not retrieve anchor text, link is embedded";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:4;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:62:"http://us2.php.net/get/php-5.2.6.tar.gz/from/us.php.net/mirror";s:4:"host";s:11:"us2.php.net";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:48:"Could not retrieve anchor text, link is embedded";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:5;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:36:"http://bugs.php.net/bug.php?id=44991";s:4:"host";s:12:"bugs.php.net";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:18:"php.net bug# 44991";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:6;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:45:"http://bugs.gentoo.org/show_bug.cgi?id=223891";s:4:"host";s:15:"bugs.gentoo.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:24:"Gentoo Linux bug #223891";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:7;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:115:"http://overlays.gentoo.org/proj/php/browser/patches/php-patches/5.2.6/php5/freetds-compat.patch?rev=3488&format=raw";s:4:"host";s:19:"overlays.gentoo.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"here";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:8;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:26:"http://www.phpmsadmin.org/";s:4:"host";s:14:"phpmsadmin.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:14:"phpmsadminÂ ";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:9;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:31:"http://www.symfony-project.org/";s:4:"host";s:19:"symfony-project.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:7:"Symfony";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - PHP
  - St.Louis
  - Technology

---
Once in a while in my high level application stack, web development world, I am thrown for a loop, and I have to venture down into the bowls of the LAMP stack, or MAMP stack in my case.Â  A client for the company I work for <a target="_blank" href="http://jwebmedia.com">jWeb</a> has a desktop application that their entire company uses all day every day.Â  This application is a win32 desktop application that is tied to a SQL Server 2005 database.Â  We are tasked with building a web application that ties directly to this database, and adds our own custom special sauce to the mix.Â  Needless to say the Microsoft Development platform is very windows centric, so I looked to an open source solution.Â  As I usually do when I search for a software solution to my problems, I found a champion, <a target="_blank" href="http://freetds.org">FreeTDS</a>.Â  This software library allows linux (and therefore Mac OSX&#8230; freebsd is not linux I know) to be able to connect directly, not through ODBC, to SQL Server and execute sql statements (Stored Procedures too!!)

To give context to this solution, here is my current developer web server setup:

  * Mac Powerbook G4 running OSX 10.4.11
  * Apache/2.2.4
  * PHP 5.2.5
  * MySql 5.0.18

And here is my SQL Server Set Up

  * Windows XP SP3
  * SQL Server 2005 Developer Edition

Couple of pitfalls to watch out for here with regards to your SQL Server Development machine:

  * Make sure that SQL Server is running an listening via TCP/IP.

  * There are multiple ways of running SQL Server (Shared Memory, Named Pipes, TCP/IP, VIA), and it is essential that you have TCP/IP <span style="font-weight: bold">ENABLED</span>.Â  I don&#8217;t know if it comes by default with TCP / IP disabled, but it was on mine so this will kill you before you start if you dont have this sorted out.
  * Change these settings by going to Start > Programs > Microsoft SQL Server 2005 > Configuration Tools > SQL Server Configuration Manager
  * Click on SQL Server 2005 Network Configuration
  * Make sure that TCP / IP is enabled.Â  You might have to restart SQL Server from the Services Panel in Windows Control Panel.
  * Make sure that you have Windows Firewall allowing port 1433 (default sql server port) or whatever you have it set to.
  * Here is the dooosey.Â  If you have a Cisco VPN client installed on this machine, there comes with it a Firewall, that will kill all port traffic.Â  This runs even when the VPN client is not currently connected.Â  To disable this, bring up the VPN client connection window.Â  A System tray icon will pop up for Cisco VPN, there is an option for &#8220;Stateful Firewall, (Always On)&#8221;Â  make sure this is <span style="font-weight: bold">UNCHECKED</span>.

Ok, before we can upgrade to FreeTDS and compile it with connections to SQL Server we need to download the FreeTDS library.

Download from [here][1] (ftp://ftp.ibiblio.org/pub/Linux/ALPHA/freetds/stable/freetds-stable.tgz).

Run these commands:

  1. cd /usr/local/src
  2. wget ftp://ftp.ibiblio.org/pub/Linux/ALPHA/freetds/stable/freetds-stable.tgz
  3. tar zxf freetds-stable.tgz
  4. cd freetds-0.82
  5. ./configure
  6. make
  7. sudo make install

This will install FreeTDS to you /usr/local directory.Â  It is important to put it in this location, cause of the following next steps.  
Ok now, lets upgrade to 5.2.6 PHP.

Grab the source code from PHP.net.

Follow these steps:

  1. cd /usr/local/src
  2. wget http://us2.php.net/get/php-5.2.6.tar.gz/from/us.php.net/mirror
  3. tar zxf php-5.2.6.tar.gz
  4. cd php-5.2.6

Ok now here is the fun <font size="4">fun</font> <font size="5">fun</font>.

FreeTDS decided in release 0.82 to change the way that it installs its compiled libs.Â  PHP (as of 5.2.6) has not release an official update to this problem.Â  FreeTDS.org/news.html has recommended adding dummy files to allow the PHP extensions (mssql, pdo_dblib) to compile correctly.Â  This soution is not really solving the problem, so I looked to the PHP developers to see if there is a better solution.

Low and behold, there was!

Two different links:

  1. [php.net bug# 44991][2]
  2. [Gentoo Linux bug #223891][3]

These two sites discuss the problem in depth.Â  The great news, they provided a Patch to solve the problem!

Download it [here][4]. (http://overlays.gentoo.org/proj/php/browser/patches/php-patches/5.2.6/php5/freetds-compat.patch?rev=3488&format=raw)

Copy the patch file to your php src directory (/usr/local/src/php-5.2.6).

Run these commands:

  1. patch -p0 -iÂ  /usr/local/src/php-5.2.6/freetds-compat.patch

  1. Since it is in interactive mode type these two file locations

  1. ext/mssql/config.m4
  2. ext/pdo_dblib/config.m4

This will patch the source code problems with FreeTDS 0.82 and PHP 5.2.6

Now compile php (based off of my settings):

  1. &#8216;./configure&#8217; &#8216;&#8211;prefix=/usr/local/apache2/php&#8217; &#8216;&#8211;with-zlib&#8217; &#8216;&#8211;with-dom=/sw/&#8217; &#8216;&#8211;with-libxml-dir=/sw/&#8217; &#8216;&#8211;with-xsl=/sw/&#8217; &#8216;&#8211;with-jpeg-dir=/sw&#8217; &#8216;&#8211;with-libtiff-dir=/sw&#8217; &#8216;&#8211;with-png-dir=/sw&#8217; &#8216;&#8211;with-mysql=/usr/local/mysql/&#8217; &#8216;&#8211;with-apxs2=/usr/local/apache2/bin/apxs&#8217; &#8216;&#8211;with-curl&#8217; &#8216;&#8211;enable-exif&#8217; &#8216;&#8211;with-ttf&#8217; &#8216;&#8211;with-freetype-dir=/usr/X1186&#8217; &#8216;&#8211;enable-bcmath&#8217; &#8216;&#8211;with-iconv&#8217; &#8216;&#8211;with-gd&#8217; &#8216;&#8211;with-t1lib=/sw&#8217; &#8216;&#8211;enable-gd-native-ttf&#8217; &#8216;&#8211;with-xpm-dir=/usr/X11R6/lib&#8217; &#8216;&#8211;with-openssl=/sw/&#8217; &#8216;&#8211;enable-ftp&#8217; &#8216;&#8211;enable-soap&#8217; &#8216;&#8211;with-xmlrpc&#8217; &#8216;&#8211;with-mysqli=/usr/local/mysql/bin//mysql\_config&#8217; &#8216;&#8211;with-mssql=/usr/local&#8217; &#8216;&#8211;enable-zip&#8217; &#8216;&#8211;with-imap=/usr/local/imap&#8217; &#8216;&#8211;with-imap-ssl=/sw&#8217; &#8216;&#8211;with-kerberos&#8217; &#8216;&#8211;enable-mbstring&#8217; &#8216;&#8211;with-mcrypt=/sw&#8217; &#8216;&#8211;with-pdo-mysql=/usr/local/mysql/bin/mysql\_config&#8217; &#8216;&#8211;with-pdo-dblib=/usr/local&#8217; &#8216;&#8211;enable-pdo&#8217;
  2. make
  3. sudo make install

You are off to the races!!!

You can now install open source tools such as:

  *  [phpmsadminÂ ][5]
  * [Symfony][6] with Doctrine / Propel ORM systems

I plan to use both, but Symfony will allow me to read the schema directly from the SQL Server, and build out ORM objects based on their schema!!!

Good luck!

P.S. Dont forget to restart Apache!!! PHP lives in memory based on the last apache restart, so you wont see changes reflected until you force restart apache.

 [1]: ftp://ftp.ibiblio.org/pub/Linux/ALPHA/freetds/stable/freetds-stable.tgz
 [2]: http://bugs.php.net/bug.php?id=44991
 [3]: http://bugs.gentoo.org/show_bug.cgi?id=223891
 [4]: http://overlays.gentoo.org/proj/php/browser/patches/php-patches/5.2.6/php5/freetds-compat.patch?rev=3488&format=raw
 [5]: http://www.phpmsadmin.org/
 [6]: http://www.symfony-project.org/