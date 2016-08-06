---
layout: post
title: "python pickle 模块简要介绍"
comments: true
keywords: "python"
category: python
author: "leilyzhang"
---

### 认识 pickle 序列化

序列化的概念很简单。内存里面有一个数据结构，你希望将它保存下来，重用，或者发送给其他人。你会怎么做？嗯, 这取决于你想要怎么保存，
怎么重用，发送给谁。很多游戏允许你在退出的时候保存进度，然后你再次启动的时候回到上次退出的地方。(实际上, 很多非游戏程序也会这么干
。) 在这个情况下, 一个捕获了当前进度的数据结构需要在你退出的时候保存到磁盘上，接着在你重新启动的时候从磁盘上加载进来。这个数据只会
被创建它的程序使用，不会发送到网络上，也不会被其它程序读取。因此，互操作的问题被限制在保证新版本的程序能够读取以前版本的程序创建的
数据.

在这种情况下，pickle 模块是理想的。它是Python标准库的一部分, 所以它总是可用的。它很快; 它的大部分同Python解释器本身一样是用C写的.
它可以存储任意复杂的Python数据结构.

### 什么东西能用pickle模块存储?

所有Python支持的 原生类型 : 布尔, 整数, 浮点数, 复数, 字符串, bytes(字节串)对象, 字节数组, 以及 None.
由任何原生类型组成的列表，元组，字典和集合.
由任何原生类型组成的列表，元组，字典和集合组成的列表，元组，字典和集合(可以一直嵌套下去，直至Python支持的最大递归层数).
函数，类，和类的实例(带警告).


### 示例

```python
#!/usr/bin/env python
import pickle
account_info = {

        87878779 : ['password1',15000,15000,'Normal'],
        76881162 : ['password2',12000,12000,'Lock']
}
f = file('accout.pki','wb')
pickle.dump(account_info, f)
f.close()
f = file('accout.pki','wb')
account_info[87878779][0] = 'password111111'
pickle.dump(account_info, f)
f.close()
```

>注意： 当修改了字典，再次dump 进去，此时pki文件 将有2个字典，因此为了保证唯一性，需要每次序列号dump时，关闭文件，再打开。当修改了字典，再次dump 进去，此时pki文件 将有2个字典，因此为了保证唯一性，需要每次序列号dump时，关闭文件，再打开。

