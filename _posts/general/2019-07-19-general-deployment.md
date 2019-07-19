---
layout: post
title:  "Deployment related"
subtitle: "All kinds of deployment strategies"
date:   2019-07-19
categories: general
permalink: /category/general/customize
---

These are some deployment strategy plus my personal thoughts

> 1. Blue/Green deployment

Need to have two identical environments. Let's call it `blue` and `green` enviroments. `Blue` is normally running. Upgrade `green` environments to the target version, switch network traffics to it, test it. If it is working propertly, upgrade `blue` to the corresponding version as well. 

### Pros
- 0 Downtime
- Low risk. Can easily rollback to previous stage

### Cons
- Cost increase.
- Need to handle those unfinished transactions when switching network traffic

> **2. Gray publish**

### Reqirement

### Pros


### Cons





