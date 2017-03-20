---
layout: post
title: "Facebook Script" - 20.03.2017
---

#"Facebook Script" Selenium Webdriver Automation test - simple example



<br># 1. Script accept all new friends
<br># 2. Send 5 invites to "People You May Know"
<br># 3. Invite friends to like your fanpage
<br># Working only on polish language version

<br>#"Facebook Script" Selenium Webdriver Automation test
<br>from selenium.common.exceptions import ElementNotVisibleException
<br>from selenium.common.exceptions import NoSuchElementException
<br>from selenium import webdriver
<br>import time
<br>
<br># Start Firefox session
<br>driver = webdriver.Firefox()
<br>driver.implicitly_wait(30)
<br>driver.maximize_window()
<br>
<br>#Go to Facebook
<br>driver.get("https://www.facebook.com/friends/requests/?fcref=jwl")
<br>
<br>#Log in
<br>email = driver.find_element_by_id("email")
<br>email.send_keys("youremail")
<br>password = driver.find_element_by_id("pass")
<br>password.send_keys("yourpassword")
<br>
<br>#Loginbutton submit
<br>loginbutton = driver.find_element_by_id("loginbutton")
<br>loginbutton.submit()
<br>print("You are log in")
<br>
<br>#Accept new friends
<br>myinvites = driver.find_elements_by_xpath("//div[@class='ruResponseButtons']/button[contains(text(), 'Potwierd')]")
<br>newinvites = str(len(myinvites))
<br>print ("Found " + newinvites + " friends to accept")
<br>time.sleep(2)
<br>#Friends accepting
<br>invitenumber = int(newinvites)
<br>if (invitenumber > 0):
<br>    time.sleep(3)
<br>    for myinvite in myinvites:
<br>        myinvite.click()
<br>        print("Friend accepted")
<br>else:
<br>    print("No invites from Friends")
<br>
<br>#Invite new friends
<br>i=0
<br>friendbuttons = driver.find_elements_by_xpath("//*[@class='uiList _4kg _6-h _6-j _4ks']//button[contains(text(), 'Dodaj')]")
<br>for friendbutton in friendbuttons:
<br>    # check for popup
<br>    try:
<br>        time.sleep(3)
<br>        driver.find_element_by_link_text('Zamknij').click()
<br>        print ('Popup closed')
<br>    except (ElementNotVisibleException, NoSuchElementException):
<br>        friendbutton.click()
<br>        i = i + 1
<br>        print("Add " + str(i) + " friend")
<br>        if (i > 5):
<br>         break
<br>         
<br>
<br>print ("Invite friends to like your fanpage")
<br>driver.get("Link to your fanpage")
<br>time.sleep(2)
<br>addfanpagefrs = driver.find_elements_by_xpath("//button[@class='_4jy0 _4jy3 _517h _51sy _42ft']")
<br>time.sleep(1)
<br>for addfanpagefr in addfanpagefrs:
<br>    addfanpagefr.click()
<br>    print("Friend added")
<br>
<br>print("The End :)")


https://github.com/yoshura/Selenium-Webdriver-scripts/blob/master/Facebook%20script%202


