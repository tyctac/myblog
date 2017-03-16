---
layout: post
title: my conclusion for some circmustance
categories:
- Programming
tags:
- conclusion
---

#### 一些总结
- 循环初始，考虑清楚

#### 有限状态机（dfa）
1. 确定转移条件  
2. 确定状态个数，合法终结状态，标记一个非法状态（最终要加上这个状态在状态转移举证中）  
状态转移矩阵的获得:除了一个非法状态，其他都是合法状态,横坐标是状态，纵坐标是转移条件，值是转移之后的状态--->valid number:![问题](http://www.cnblogs.com/zuoyuan/p/3703075.html),几个状态：1->4，非法字符也是一个转移条件，不能漏掉，转移到非法状态  
不要弄混非法状态和中间状态  

#### 基尼指数-->**抽样建模** 

