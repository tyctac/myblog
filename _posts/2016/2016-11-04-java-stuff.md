---
layout: post
tittle: java stuff
categories:
- programming
tags:
- javascript
---
# java reflection
- 用泛型存储取出来后不能用，（存储的对象中含有包含另一个对象的list）只好用更死板的方法，只是应为没有预先分配存储空间而已。。。
# hibernate java
```
Session session = HibernateUtil.currentSessioin();
Transaction tran = session.beginTransaction();
.....
tran.commit();
```

