---
layout: post
title:  "Kafka vs Pulsar"
date:   2019-09-17
tags:
  - message queue
---

# Kafka vs Pulsar

> This is a note and also my personal understanding about these two mainly being used message queue. 

A artical talks about the difference between these two, you can click [here](https://kafkaesque.io/7-reasons-we-choose-apache-pulsar-over-apache-kafka/)

1. Kafka stores everthing in its log, which is append-only, while Pulsar stores its data in a distrubuted store service - Apache BookKeeper. The drawback of the way how Kafka handles log is that when the log file is really big, and the broker is down, if you are adding a new broker, the broker needs to sync data for the dead broker, it will takes a long time. 

2. Becasuse of #1, Kafka's broker is stateful and Pulsar's broker is stateless as it does not contains any data inside. Pulsar can scale streamlessly.

3. Kafka's log can getting really big while Pulsar's log won't be that big because Pulsar will delete it is log. 
    - Pulsar has two types of topics `persistent` and `non-persistent`. The only difference between these two is about those messages that are not `ackownledged` (Concusmer will acknowledge messages when it received). Which means all messages that are consumed will be deleted. 

    - Kafka does not delete messages in topic after they are consumed. 

    - **The drawback of Pulsar is you cannot add more consumer on-demand, as it will be deleted by broker.** This means you cannot use Pulsar in a `Event Sourcing` architecture. 

In general, both have their suitable scenario. For an `event sourcing` architecure, Kafka is your choice. 
