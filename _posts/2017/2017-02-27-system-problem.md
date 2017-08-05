---
layout: post
title: interesting thought  
category: 
- Linux  
tags:
- records
- ideas
---

**进程通信问题**  
- xmanager 中vi打开.md文件不能打开浏览器，应该与vi的插件实现方式有关吧

**编码问题**
python 默认decode是ascii方式，[参考](https://python.jobbole.com/81246/)  
为某一个字符串加密时怎么样才能确定该字符串的原始编码？？？--->多次查询没有比较好的结果，


**很蛋疼的问题**  
nexuiz-data老是安装不上,老是提示这个包安装极为不妥,使用dpkg --status 查看依赖之后安装依赖安装不成功,仍然提示这个错误,卸载也卸载不掉,最后终于解决,感谢网上的大神:
```
sudo dpkg --remove --force-remove-reinstreq bioinfoserv-eioffice2007
```
reference:https://forum.ubuntu.com.cn/viewtopic.php?t=67359
