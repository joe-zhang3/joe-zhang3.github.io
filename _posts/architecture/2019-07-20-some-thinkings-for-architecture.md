---
layout: post
title:  "Thinkings for architectures(WIP)"
subtitle: ""
date:   2019-07-20
tags:
  - architecture
---

These are a list of architecture related ideas. Audience is not limited to dev, but all kinds of technology related people.

- **KISS** (Keep it simple or stupid). 尽量把软件设计的简单一些，傻瓜一些
- **YAGNI** (You are't gonna need it). 别手欠去耍小聪明的设计一些现在并不需要的功能
- **Crawl, Walk, Run** (Make it work, make it better, make it greater). 跟小孩学走路一样，先爬，再走，再跑。
- **Automation Test** 自动化测试是构建稳定，高质量软件的重要途径。
- **RoI** (Return of Investment). 考虑你的投资回报率，把好钢用在刀刃上
- 设计和测试尽量分开。测试随着开发进度走，而不是等开发完了一起测试

- **MVP** (minimal viable product) 你永远无法想象客户是怎么使用你的产品的。 先做出来的东西给他看，根据回馈来修改你的产品
- 尽可能少做新功能。对于有疑问的就别做，当然尽可能留一些扩展点

- 需要了解硬件，操作系统，到你的语言平台，这样才能做出更好的架构
- **Amdahl Law** (大意为系统可并行化程度越高，多核越能发挥作用，废话) 多使用异步处理，比如immutable的数据，并行计算，尽量不要使用锁
- 对于一个non-blocking, event driven的系统而言，不要使用锁或其他的IO操作，它会使你的系统慢的跟马一样

- 设计无状态系统，尽量使用`Shared Nothing Architecture`.
- 不能可能实现 `exactly once delivery`. 凡是宣称能达到`exactly once delivery`的肯定在某些地方做了限制.
- 尽可能的把你的系统设计成`幂等`的，这样至少可以实现 `at least once delivery` 

- `CAP Theorem`. Consistency, Availability, Partition Tolerance, pick any two. 

