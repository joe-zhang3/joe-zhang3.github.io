---
layout: post
title:  "DDoS attack"
date:   2019-08-29
tags:
  - DDoS
---

> Talk about DDoS attack and ways to prevent it. 

## What is DDoS attack?

> In computing, a denial-of-service attack (DoS attack) is a cyber-attack in which the perpetrator seeks to make a machine or network resource unavailable to its intended users by temporarily or indefinitely disrupting services of a host connected to the Internet. Denial of service is typically accomplished by flooding the targeted machine or resource with superfluous requests in an attempt to overload systems and prevent some or all legitimate requests from being fulfilled

While DDoS means `distributed denial-of-service attack`

### Three main types of DDoS attack

1. Volumetric Attacks.
  - Attackers just send as many requests as they can to a single server, occupy all open ports of this server.

2. Application-Layer Attacks
  - Attackers send floods of requests to the application. Application is busy with these requests and not able to process other legitimate requests.

3. Protocol Attacks
  - Mainly like SYN flood, client sends syn to server, server reponses syn-ack, and waiting for the ack fromm client, which never happens. 

## Best practicases to prevent DDoS attack