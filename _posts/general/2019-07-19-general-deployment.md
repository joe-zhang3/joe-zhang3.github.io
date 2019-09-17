---
layout: post
title:  "Deployment related(WIP)"
subtitle: "All kinds of deployment strategies"
date:   2019-07-19
---

> This is a note for popular deployment strategies plus my personal thoughts

# Blue/Green deployment

Need to have two identical environments. Let's call it `blue` and `green` enviroments. `Blue` is normally running. Upgrade `green` environments to the target version, switch network traffics to it, test it. 

> Pros

- 0 Downtime
- Low risk. Can easily rollback to previous stage

> Cons

- Cost increase.
- Need to handle unfinished transactions when switching network traffic

# Gray publish (Canary releases)

Pick some candidates out, deploy the new version those those candidate(s), QA verify the change and deploy the change to all left servers/pods if QA shine the green light on. 


# Rolling release

Gradually deploy versions to servers/pods. 



