---
title: Apache 2.2.3 and PHP 5.1.5 curl 7.15.5 Compiled on Powerbook G4 17″
author: Ben Wann
type: post
date: 2006-08-25T15:50:29+00:00
url: /2006/08/25/apache-223-and-php-515-curl-7155-compiled-on-powerbook-g4-17/
wpil_sync_report3:
  - 1
wpil_links_inbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_internal_count_data:
  - 'a:0:{}'
wpil_links_outbound_external_count:
  - 3
wpil_links_outbound_external_count_data:
  - 'a:3:{i:0;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:19:"http://curl.haxx.se";s:4:"host";s:12:"curl.haxx.se";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:19:"http://curl.haxx.se";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:1;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:53:"http://www.devlib.org/apache/httpd/httpd-2.2.3.tar.gz";s:4:"host";s:10:"devlib.org";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:18:"httpd-2.2.3.tar.gz";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}i:2;O:15:"Wpil_Model_Link":8:{s:7:"link_id";i:0;s:3:"url";s:57:"http://us2.php.net/get/php-5.1.5.tar.bz2/from/this/mirror";s:4:"host";s:11:"us2.php.net";s:8:"internal";b:0;s:4:"post";N;s:6:"anchor";s:4:"here";s:15:"added_by_plugin";b:0;s:8:"location";s:7:"content";}}'
wpil_sync_report2_time:
  - 2023-01-04T23:31:48+00:00
categories:
  - Nerd
  - St.Louis
  - Technology

---
Finally got my powerbook re-setup using the latest and greatest from PHP, Apache, and libcurl. (of course all of the other goodness as well)

Here is the order:

  1. **Curl**. If you need a new version of curl and libcurl installed: go here <http://curl.haxx.se>.  
    You will need to compile from source. Important note here: Make sure that you dont have another version of curl that can be read from the $PATH. (This becomes important when compiling PHP in a few minutes) 
  2. **Apache**. Download the source from [httpd-2.2.3.tar.gz][1]  
    Now follow these steps:</p> 
      1. `./configure --enable-mods-shared=all`
      2. sudo make
      3. sudo make install
    
    It is good to note that since I didn&#8217;t specify a prefix (such as &#8211;prefix=/usr/bin/) that the configuration script will choose the default install location (/usr/local/apache2)

  3. **PHP**. Now it is time to compile PHP. Download the source from [here][2] (From the us2.php.net mirror off of sourceforge).  
    Now follow these steps:</p> 
      1. `<br />
./configure<br />
--prefix=/usr/local/apache2/php<br />
--with-zlib<br />
--with-dom=/sw/<br />
--with-libxml-dir=/sw/<br />
--with-xsl=/sw/<br />
--with-jpeg-dir=/sw/<br />
--with-png-dir=/sw/<br />
--with-mysql=/usr/local/mysql/<br />
--with-apxs2=/usr/local/apache2/bin/apxs<br />
--with-gd<br />
--with-curl<br />
` 
      2. sudo make
      3. sudo make install
    
    It is good to note here, that I had installed a version of curl on my machine and made sure that when I accessed the $PATH, that I was addressing the correct version.

I have done this all before, but each time I do it, I learn something new. Hope this can help someone out there who is banging their head.

Happy compiling!

<!--296a9eef3d4dcc227d18f519c3ecae32--></p> 

<!--0c557dc482d6b5f041452a3a280815e8-->

<!--e2154b12384a479550391b9f88170446-->

 [1]: http://www.devlib.org/apache/httpd/httpd-2.2.3.tar.gz
 [2]: http://us2.php.net/get/php-5.1.5.tar.bz2/from/this/mirror