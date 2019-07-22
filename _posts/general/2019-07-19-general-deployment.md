---
layout: post
title:  "Deployment related"
subtitle: "All kinds of deployment strategies"
date:   2019-07-19
categories: general
permalink: /category/general/customize
---

> This is a note for popular deployment strategies plus my personal thoughts

# Blue/Green deployment

Need to have two identical environments. Let's call it `blue` and `green` enviroments. `Blue` is normally running. Upgrade `green` environments to the target version, switch network traffics to it, test it. 

> Pros

- 0 Downtime
- Low risk. Can easily rollback to previous stage

> Cons

- Cost increase.
- Need to handle those unfinished transactions when switching network traffic

# Gray publish

### Reqirement

### Pros


### Cons





