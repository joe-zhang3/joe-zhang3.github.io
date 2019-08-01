---
layout: post
title:  "Best practice for writting unit tests"
date:   2019-07-24
categories: general
permalink: /category/general/best-practice-to-write-unit-tests
tags:
  - unit test
---

> Some thoughts for writting UT friendly code or how to write your unit test. 


## 1. Do NOT rely on environment for your unit tests.

e.g. do not try to connect to a real database.

```csharp
public EMCUnityConnectorTest()
{

    _instance = new ConnectorInstance()
    {
        Endpoint = "https://10.148.9.40",
        UserName = "atom",
        PasswordHash = "kasNMFdKC/+C/qwan3Eu7PT440byo8Lwe3dYKbWQgqQyz8dG3fD0bdSJi+87gdxO",
        Id = Guid.Parse("5B32CF84-F39E-4AE6-8447-508FBAF423F5"),
        ConnectorTypeId = Guid.Parse("89DB00D6-4F17-444E-A4EA-F527D6FFB390")
    };

    _logger = new MockLogger();

    _connector = new EMCUnityConnector();
    _connector.Initialize(_instance, _logger);

}

[Fact]

public void ConnectTest()
{
    var success = _connector.Connect();
    Assert.True(success);
}

```

## 2. Field injection is NOT recommended.

This means `@Autowired` annotation should not be applied to a field. Check more details via [this](https://stackoverflow.com/questions/39890849/what-exactly-is-field-injection-and-how-to-avoid-it) link.

        
```java
public class Bar{
    @Autowired
    private Foo foo;

    public void doWork(){
        foo.doSomething;
    }
}

```

Use constructor instead


```java
public class Bar{
    private Foo foo;

    @Autowired
    public Bar(Foo foo){
        this.foo = foo;
    }

    public void doWork(){
        foo.doSomething();
    }
}
```

**If you are going to write a unit test for the `doWork` method, you will not be able to mock the `foo` without the help of Spring IoC container.**

## 3. Follow `Dependency Inversion` princple strictly. 

> - High-level modules should not depend on low-level modules. Both should depend on abstractions (e.g. interfaces).
> - Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

Which in general means, use `interface` or `abstract class` as much as possible, or use `IoC` containers

## 4. Follow `Single Responsibility` princple strictly. 

Your method should handly only one thing, should be used for only one purpose.


## 5. How to handle legacy code?

You are commonly facing a problem that it is pretty hard to write unit test for legacy code, which does not follow rules mentioned above. `Refactor` is the only recommend way to fix that issue, but for sure, it takes time.