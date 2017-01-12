---
layout: post
title: Dating Script v3.25 - SQL Injection - 11.01.2017
---

An attacker can exploit this vulnerability to read from the database. The parameter 'id' is vulnerable.

https://www.exploit-db.com/exploits/41027/

<br># Vulnerability: Dating Script v3.25 - SQL Injection
<br># Date: 11.01.2017
<br># Software link: http://itechscripts.com/dating-script/
<br># Demo: http://dating.itechscripts.com
<br># Price: 199$
<br># Category: webapps
<br># Exploit Author: Dawid Morawski
<br># Website: http://www.morawskiweb.pl
<br># Contact: dawid.morawski1990@gmail.com
<br>#######################################
 
 
<br>1. Description
<br>An attacker can exploit this vulnerability to read from the database.
<br> 
<br>2. SQL Injection / Proof of Concept:
<br>Vulnerable Parameter: id
<br>http://localhost/[PATH]/see_more_details.php?id=[SQL]
