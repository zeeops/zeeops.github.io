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

$path = "C:\Windows\Temp\Softwares\tools\" $softwares = Import-Csv "C:\Users\admin\Desktop\automation\aplications.csv" -Delimiter "," -Header 'Installer' , 'Switch' , 'Link' | Select-Object Installer,Switch,Link Write-Output $softwares foreach($link in $softwares){ $url = $link.Link $url = $url.ToString() $filename = $link.Installer $filename = $filename.ToString() Write-Output $url mkdir C:\Windows\Temp\Softwares\tools -Force #$dir = 'C:\Windows\Temp\Softwares\tools\' Write-Host "Downloading $url" Write-Output "filename" $filename $dlPath = $path + $filename Write-Output "dlpath" $dlPath Write-Output "link" $url Invoke-WebRequest $url -OutFile $dlPath } foreach($software in $softwares){ $softexec = $software.Installer $softexec = $softexec.ToString() Write-Output $softexec $pkgs = Get-ChildItem $path$softexec | Where-Object {$_.Name -eq $softexec} foreach($pkg in $pkgs){ $ext = [System.IO.Path]::GetExtension($pkg) $ext = $ext.ToLower() $switch = $software.Switch $switch = $switch.ToString() Write-Output $switch if($ext -eq ".msi"){ mkdir C:\Windows\Temp\Softwares -Force Copy-Item "$path$softexec" -Recurse C:\Windows\Temp\Softwares -Force Write-Host "Installing $softexec silently, Please wait...." -BackgroundColor Yellow Start-Process "C:\Windows\Temp\Softwares\$softexec" -ArgumentList "$switch" -Wait Remove-Item "C:\Windows\Temp\Softwares\$softexec" -Recurse -Force Write-Host "Installation of $softexec completed" -BackgroundColor Green } else { mkdir C:\Windows\Temp\Softwares -Force Copy-Item "$path$softexec" -Recurse C:\Windows\Temp\Softwares -Force Write-Host "Installing $softexec silently, Please wait...." -BackgroundColor Yellow Start-Process "C:\Windows\Temp\Softwares\$softexec" -ArgumentList "$switch" -Wait -NoNewWindow Remove-Item "C:\Windows\Temp\Softwares\$softexec" -Recurse -Force Write-Host "Installation of $softexec completed" -BackgroundColor Green } } }





<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg1NDUxNzg5NiwtOTI0NzE2ODgxLDEwMT
I1MzkwODUsMTYzNDI3MTczNCwxNDE3MDQ1OTQ0LC01NTQzMjA1
OCwtNjIzNDUyNzQzLC02MDY0MjkwMzUsNTIxNzUxMzkxLC00Mj
UwNzI5MjQsMTUwOTk2NTM2MSwtMTcwODE4NzI4OSwtMjExMDAy
MzQ2M119
-->