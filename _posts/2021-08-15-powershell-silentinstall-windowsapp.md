---
title: "Power shell script to install remote exe file silently"
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

Prometheus is a monitoring tool that stores time series data such as metrics. Grafana is used to visualise the data in Prometheus, whereas alert manager is used to send out alerts.

I'll demonstrate how to set up VMware Exporter to connect to VMware vCenter and retrieve all metrics on Prometheus.
Basic Alerting rule for exporter

> Exporter used for connecting vmware Vcenter:
> [https://github.com/pryorda/vmware_exporter](https://github.com/pryorda/vmware_exporter)

vm guest machine :

    groups:
	  - name: memory
	    rules:
		  - alert: VirtualMachineMemoryWarning
		    expr: vmware_vm_mem_usage_average / 100 >= 80
		    for: 5m
		    labels:
			  severity: warning
			  team: devops
		    annotations:
			  summary: Virtual Machine Memory Warning (instance {{ $labels.instance }})
			  description: High memory usage on {{ $labels.instance }}


All alerting rules are placed on my git repo

> [https://github.com/zeeops/vmware_exporter.git](https://github.com/zeeops/vmware_exporter.git)





<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYzNDI3MTczNCwxNDE3MDQ1OTQ0LC01NT
QzMjA1OCwtNjIzNDUyNzQzLC02MDY0MjkwMzUsNTIxNzUxMzkx
LC00MjUwNzI5MjQsMTUwOTk2NTM2MSwtMTcwODE4NzI4OSwtMj
ExMDAyMzQ2M119
-->