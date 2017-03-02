---
layout: post
title: Facebook status poster - Selenium Webdriver -  02.03.2017
---

"Facebook status poster" Selenium Webdriver Automation test - simple example 

<br>from selenium import webdriver
<br>import time
<br>
<br># Start Firefox session
<br>driver = webdriver.Firefox()
<br>driver.implicitly_wait(30)
<br>driver.maximize_window()
<br>
<br>#Go to Facebook
<br>driver.get("http://www.facebook.pl")
<br>
<br>#Log in 
<br>email = driver.find_element_by_id("email")
<br>email.send_keys("Youremail@")
<br>password = driver.find_element_by_id("pass")
<br>password.send_keys("Your password")
<br>
<br>#Loginbutton submit
<br>loginbutton = driver.find_element_by_id("loginbutton")
<br>loginbutton.submit()
<br>
<br>#Send post
<br><br>newpost = driver.find_element_by_css_selector("[name='xhpc_message']")
<br>newpost.click()
<br>newpost.send_keys("Hello test!")
<br>newpost.submit()
<br>
<br>driver.close()


