---
title: "How To Monitor Vmware vcenter with Prometheus"
excerpt: ""
header:
    #overlay_image: /assets/images/writinghabit.jpg
    #caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
    #cta_label: "More Info"
    #cta_url: "https://unsplash.com"
    overlay_filter: 0.25
    teaser: /assets/images/post_images/vmwareexporter.png
categories:
  - monitoring
tags:
  - Prometheus
  - vmware
date: 2021-01-15
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
vm guest machine :



<p><img src="{{site.baseurl}}/assets/images/post_images/vmwareexporter.png" alt="" class="align-center" /></p>
<figcaption></figcaption>


<!--stackedit_data:
eyJoaXN0b3J5IjpbNjA5OTE2OTUzLDE1MDk5NjUzNjEsLTE3MD
gxODcyODksLTIxMTAwMjM0NjNdfQ==
-->