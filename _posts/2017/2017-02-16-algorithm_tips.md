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

#### 有用的技巧
**python**  
min(list,key),list是需要比较的数组,key是作用于list中每个元素的函数,min返回函索返回值最小的那个原始list中的对应元素  
enumerate(iterable[,start]) -> iterator for index,value of iterable  

