---
layout: post
title: some things need to be remmember in my project
category: 
- Programming
tags:
- records
---

#### 工程中遇到的一些问题
webclasy:
- 执行项目文件是遇到相对路径时会按照当前的项目入口文件的地址来处理相对路径，eg：之后补充  

**mongodb**集合设计问题
尽可能抽象，放入一个大集合，关键存储信息的字段可以作为抽象集合的一个属性，便不用担心扩展性问题  
经过测试，mongodb中  
```skip()```函数起始地址为一，也就是说，```skip(k)```意味着跳过前面k条记录进行查询
