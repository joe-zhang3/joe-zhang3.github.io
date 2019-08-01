---
layout: post
title:  "Autowired(WIP)"
subtitle: "When and how to use autowired in Spring"
date:   2019-07-21
categories: general
permalink: /category/general/autowired
tags: 
  - spring
---

> Some ideas for when and how to use `Autowired` annotation in Spring

There are three types of injections withing Spring framework. 

   - Constructor Injection.
   - Setter Injection.
   - Field Injection.

1. Constructor Injection
  ```java
    public class Bar{

      private Foo foo;

      @Autowired
      public Bar(Foo foo){
        this.foo = foo;
      }
    }
  ```

2. Setter Injection
  ```java
    public class Bar{

      private Foo foo;

      @Autowired
      public setFoo(Foo foo){
        this.foo = foo;
      }
    }
  ```

3. Field Injection
  ```java
    public Class Bar{
      @Autowired
      private Foo foo;
    }
  ```

It is apparently that third way is simple, straight forward, but it has a few drawbacks. 

1. It is not friendly for unit test. As you cannot easily mock a `foo` and injected into the `bar` object.
2. You cannot inject a immutable objects, say a final object in Java.