pdnsd_win32
===========

The Windows port of pdnsd DNS server.

This is from pdnsd project (http://members.home.nl/p.a.rombouts/pdnsd/index.html).

How it works : 
   
   When you send a DNS resolve request via GFW for some host(twitter, facebook, etc), GFW will send a fake DNS result, which arrives to your computer faster than the correct package from the DNS Server (Google DNS, OpenDNS, etc). As a result, you system gets an incorrect host address.
   Luckily, GFW can only deal with UDP DNS requests, till now. So we can build a DNS cache server, which uses TCP to resolve host names.

Version :1.2.9a

Usage: 
    1. Create a cache folder. 
       For example, c:\temp.
    2. Set it in pdnsd.conf
       cache_dir="c:\\temp"; # Change it to your folder
    3. Run pdnsd:
       pdnsd -c pdnsd.conf
       If everything is OK, pdnsd service will start. 
    4. Change the DNS in Network Setting to localhost or 127.0.0.1.
    
    And that's all. Now pdnsd will resolve hosts for you.

    You can also change other parameters in pdnsd.conf.
 
    Thanks : config file is from http://leeraw.com/?p=3621
    
