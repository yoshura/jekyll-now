---
layout: post
title: "Facebook status poster" Selenium Webdriver Automation test example - 02.03.2017

---

from selenium import webdriver
import time

# Start Firefox session
driver = webdriver.Firefox()
driver.implicitly_wait(30)
driver.maximize_window()

#Go to Facebook
driver.get("http://www.facebook.pl")

#Log in 
email = driver.find_element_by_id("email")
email.send_keys("Youremail@")
password = driver.find_element_by_id("pass")
password.send_keys("Your password")

#Loginbutton submit
loginbutton = driver.find_element_by_id("loginbutton")
loginbutton.submit()

#Send post
newpost = driver.find_element_by_css_selector("[name='xhpc_message']")
newpost.click()
newpost.send_keys("Hello test!")
newpost.submit()

driver.close()

