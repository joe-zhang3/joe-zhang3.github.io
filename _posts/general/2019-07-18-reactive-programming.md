---
layout: post
title:  "Reactive Programming(TODO)"
date:   2019-07-18
categories: general
permalink: /category/general/reactive-programming
tags:
  - reactive
---

# Reactive Programming

> What's reactive programming

4 Core Concepts

- Observer
- Observable
- Hot VS. Cold Observable
- Subject Variants


~~~javascript
interface Observer{
  next: function
  error: function
  complete: function
}
~~~
