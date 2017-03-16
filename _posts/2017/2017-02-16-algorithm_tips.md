---
layout: post
title: python_algorthm_tips_string_operation
categories:
- Programming
tags
- python
- algorithm
---

**字符串**
正则表达式：获取数字：
```str = str.strip()  
str = re.findall('(^[\+\-0]*\d+)\D*',str)
```  

**时间复杂度**  
python 的类型转换，eg：set <=> list

**数组对象**  

**用'*'初始化二维数组**  
不能正常赋值的原因是，*是对对象引用的赋值，所以改变该对象会改变所有指向它的引用

#### 问题记录:在一个平面中，给出很多一样大小的正方形，然后给出很多点，要求查询每个点落在多少正方形内。kd树？？
