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
Silent switch of almost all software can be found from following website

> https://silentinstallhq.com/

    https://github.com/zeeops/powershell



<!--stackedit_data:
eyJoaXN0b3J5IjpbMjYxNjA2MjA5LDE4OTY2NTkyNDAsLTkyND
cxNjg4MSwxMDEyNTM5MDg1LDE2MzQyNzE3MzQsMTQxNzA0NTk0
NCwtNTU0MzIwNTgsLTYyMzQ1Mjc0MywtNjA2NDI5MDM1LDUyMT
c1MTM5MSwtNDI1MDcyOTI0LDE1MDk5NjUzNjEsLTE3MDgxODcy
ODksLTIxMTAwMjM0NjNdfQ==
-->