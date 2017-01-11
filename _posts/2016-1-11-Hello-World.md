---
layout: post
title: My link trader - SQL Injection 
---

An attacker can exploit this vulnerability to read from the database. The parameter 'id' is vulnerable.

https://www.exploit-db.com/exploits/41010/

![_config.yml]({{ site.baseurl }}/images/config.png)

# Vulnerability: My link trader - SQL Injection
# Date: 11.01.2017
# Vendor Homepage:
http://software.friendsinwar.com/scripts_example/my_link_trader/
# Tested on: Kali Linux 2016.2
# Author: Dawid Morawski
# Website: http://www.morawskiweb.pl
# Contact: dawid.morawski1990@gmail.com
#########################
 
#########################
# SQL Injection/POC :
# Vulnerable Parametre : id
# http://localhost/[PATH]/out.php?id=[SQL]
