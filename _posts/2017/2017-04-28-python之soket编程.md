---
layout: post  
title: python之soket编程  
categories: 
- Programming
tags:
- records
---

#### soket基本原理
1. 如图所示  
    ![](http://wx4.sinaimg.cn/mw690/bf0e799bly1ff2eqx97qrj20j20fln2c.jpg)
    解释：  
**服务端**
    1. 第一步是创建soket对象。调用socket构造函数。如：  
        socket = socket.socket(family,type)  
        family参数代表地址家族**TODO**  
        type参数代表套接字类型，可分为SOCK_STREAM（流套接字）和SOCK_DGRAM(数据报套接字）  
    2. 第二步是将socket绑定到指定地址。通过socket对象的bind方法实现：  
        socket.bind(address)  
        由AF_INET所创建的套接字，address地址必须是一个双元素元组，格式为（host,port)。host代表主机，port代表端口号。如果端口号正在使用，主机不正确或端口已被保留，bind方法将引发socket.error异常
    3. 第三步是使用socket套接字的listen方法接收连接请求。  
        socket.listen( backlog)  
        backlog指定最多允许多少客户连接到服务器。它的值至少为1.收到连接请求后，这些请求需要排队，如果队列满，就拒绝请求。   
    4. 第四步是服务器套接字通过socket的accept方法等待客户请求一个连接。  
    connection,address = socket.accept()  
    调用accept方法时，socket会进入‘waiting’状态，客户请求连接时，方法简历连接并返回服务器。accept方法返回一个含有两个元素的元组（connection，address)。第一个元素是新的socket对象，服务器必须通过它与客户通信；第二个元素address是客户的Internet地址。  
    5. 第五步是处理阶段，服务器和客户端通过send和recv方法通信，（传输 数据）。服务器调用send，并采用字符串形式向客户发送信息。send方法返回已发送的字符个数。服务器使用recv方法在从客户端接收信息。调用recv时，服务器必须指定一个整数，它对应于可通过本次方法调用来接收的最大数据量。recv方法在接收数据时会进入‘blocked’状态，最后返回一个字符串，用它表示收到的数据。如果发送的数据量超过了recv所允许的，数据会被截短。多余的数据将缓冲于接收端。以后调用recv时，多余的数据会从缓冲区删除（以及自上次调用recv以来，客户可能发送的其他任何数据）。  
    6. 传输结束，服务器调用socket的close方法关闭连接。
2. **客户端**  
    1. 创建一个socket以连接服务器：socket=socket.socket(family,type)  
    2. 使用socket的connect方法连接服务器。e.g.  
    3. 处理阶段，客户和服务器将通过send方法和recv方法通信。
    4. 传输结束，客户通过调用socket的close方法关闭连接。  
