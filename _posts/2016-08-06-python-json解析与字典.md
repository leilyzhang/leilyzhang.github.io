---
layout: post
title: "python-JSON和字典关系解析"
comments: true
keywords: "python"
category: python
author: "leilyzhang"
---

### 认识json and dict
JSON(JavaScript Object Notation) 是一种轻量级的数据交换格式。它基于JavaScript（Standard ECMA-262 3rd Edition - December 1999       ）的一个子集.JSON采用完全独立于语言的文本格式，但是也使用了类似于C语言家族的习惯（包括C, C++, C#, Java, JavaScript, Perl, Python等）。这些特性使JSON成为理想的数据交换语言.易于人阅读和编写，同时也易于机器解析和生成.

实际上JSON就是Python字典的字符串表示，但是字典作为一个复杂对象是无法直接转换成定义它的代码的字符串,需要使用eval（json 转为字典对象） 或者 json库 进行转换.


### json 模块

- 引用模块 import json 

重要函数

编码：把一个Python对象编码转换成Json字符串   json.dumps().

解码：把Json格式字符串解码转换成Python对象   json.loads().

通过python获取到json格式的字符串后，也可以通过eval函数转换成dict格式.

```python
>>> a='{"name":"yct","age":10}'
>>> eval(a)
{'age': 10, 'name': 'yct'}
```
