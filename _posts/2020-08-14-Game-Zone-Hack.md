---
layout: post
title: How-I-Hacked-GAME-ZONE
author: Sadistic
---

---

**How I Hacked GAME ZONE**

*TASK 2:

![SQL INJECTION]({{ site.baseimg }}Game-Zone/assets/XEYul1e5EY.png)

Ok so on this task we need to open your browser, I am using firefox and that is because you can get [https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/]('FoxyProxy') which will let you change your proxy settings faster
Now let move on after you get your browser open then you can go to the ip address of the deployed site it will load a site after the site is loaded your going to want to log in with an SQL INJECTION. (see code box below)

~~~
' or 1=1-- -
~~~

![SQL INJECTION]({{ site.baseimg }}Game-Zone/assets/XEYul1e5EY.png)

*TASK 3
After you login you will be presented with this page

![SQL INJECTION]({{ site.baseimg }}Game-Zone/assets/X9HKffJTqU.png)

on this page we need to intercept the search query and this is how we are going to do that

Set your browser to use burp suite as a proxy either on Chrome, Firefox, etc. (this is where [https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/]('FoxyProxy') will come in handy) which will allow you to intercept the �search� function. From this point we will copy what was intercepted from Burp Suite to a new text document.
Open Terminal. run SQLmap against the text document that was created

~~~
 sqlmap -r Text-Document.txt --dbms=mysql --dump
~~~

![sqlmap]({{ site.baseimg }}Game-Zone/assets/GwnrpZWJ96.png)

When prompted to include all tests for �MySQL� respond with �Y�, as well as all other prompts that follows.

![sqlmap-cracked-password]({{ site.baseimg }}Game-Zone/assets/4lm9tej1Zw.png)

When asked if you want to crack the password via Dictionary-based attack respond with �Y�
Utilize �Custom Dictionary File� by selecting option �2� with rockyou.txt being the Custom Dictionary File
When prompted to use Common Password Suffixes respond with �Y�
After running steps in SQLmap you should have all answers in this Task.