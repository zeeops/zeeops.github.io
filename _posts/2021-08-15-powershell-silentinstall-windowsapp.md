---
title: "Power shell script to install exe file from csv"
excerpt: ""
header:
    #overlay_image: /assets/images/writinghabit.jpg
    #caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
    #cta_label: "More Info"
    #cta_url: "https://unsplash.com"
    overlay_filter: 0.25
    teaser: /assets/images/post_images/windows_automation.png
categories:
  - powershell
  - windows
tags:
  - powershell
  - windows
  - automation
date: 2021-08-15
#last_modified_at: 2018-04-04  
author_profile: true
comments: true
share: true
featured: false
classes: wide
newsletter: false
---

This script will silently install almost any type of software on Windows. It's not a dynamic script, so don't expect it to change. It's written in such a way that you'll have to put all of your software in a.csv file, together with their quiet install switches and remote download url. Only software that supports silent installation is supported by the script. Script will detect them and silently install all of your software.

CSV file should contain 3 fields , Installer,silent switch and Download URI.
Silent switch of almost all software can be found from following
https://silentinstallhq.com/





<!--stackedit_data:
eyJoaXN0b3J5IjpbNDE0OTIwMTY4LC05MjQ3MTY4ODEsMTAxMj
UzOTA4NSwxNjM0MjcxNzM0LDE0MTcwNDU5NDQsLTU1NDMyMDU4
LC02MjM0NTI3NDMsLTYwNjQyOTAzNSw1MjE3NTEzOTEsLTQyNT
A3MjkyNCwxNTA5OTY1MzYxLC0xNzA4MTg3Mjg5LC0yMTEwMDIz
NDYzXX0=
-->