---
layout: post
title: My link trader - SQL Injection 
---

An attacker can exploit this vulnerability to read from the database. The parameter 'id' is vulnerable.

https://www.exploit-db.com/exploits/41010/

<br># Vulnerability: My link trader - SQL Injection
<br># Date: 11.01.2017
<br># Vendor Homepage: http://software.friendsinwar.com/scripts_example/my_link_trader/
<br># Tested on: Kali Linux 2016.2
<br># Author: Dawid Morawski
<br># Website: http://www.morawskiweb.pl
<br># Contact: dawid.morawski1990@gmail.com
<br>#########################
<br> 
<br>#########################
<br># SQL Injection/POC :
<br># Vulnerable Parametre : id
<br># http://localhost/[PATH]/out.php?id=[SQL]
