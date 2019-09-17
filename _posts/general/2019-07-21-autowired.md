---
layout: post
title:  "Autowired"
subtitle: "When and how to use autowired in Spring"
date:   2019-07-21
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
2. You cannot inject an immutable objects, say a final object in Java.
3. With a constructor injection, you may easily find out a code smell issue. E.g. your constructor contains more args than some static code analyzer expected (like SonarQube), then you can refator it accordingly. But with field injection issue, you will not be able to spot that.
4. It violates the encapsulation charactor of the OOP. As the IoC container is changing something which should not be changed.

In gereral, it is not recommended to use `Autowired` against to fields, but it seems like different people have different ideas, as some Spring examples also use it that way, but based on my understanding, it is not right anyway. 
