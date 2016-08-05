---
layout: post
title: "Django 日志模块 logging"
comments: true
keywords: "django"
author: "leilyzhang"
---

### Django logging 模块 


- logger提供了应用程序可以直接使用的接口；
- handler将(logger创建的)日志记录发送到合适的目的输出；
- filter提供了细度设备来决定输出哪条日志记录；
- formatter决定日志记录的最终输出格式。

### loggings
- formatters #定义日志输出格式:等级、日志信息、附加时间、进程号等等，详细日志格式参考logging官网'
- filters定义日志过滤器'
- django.utils.log.RequireDebugFalse 定义只有在环境变量DEBUG等于False时才输出日志，需要在handlers 或者logger 里面指定filters
- handlers 将(logger创建的)日志记录发送到合适的目的输出,Handlers(处理器):他来处理具体每条信息，例如是将日志打印到屏幕还是记录到文件或者发送至某个网络连接。
- oggers logger提供了应用程序可以直接使用的接口；



 - %(levelno)s: 打印日志级别的数值
 - %(levelname)s: 打印日志级别名称
 - %(pathname)s: 打印当前执行程序的路径，其实就是sys.argv[0]
 - %(filename)s: 打印当前执行程序名
 - %(funcName)s: 打印日志的当前函数
 - %(lineno)d: 打印日志的当前行号
 - %(asctime)s: 打印日志的时间
 - %(thread)d: 打印线程ID
 - %(threadName)s: 打印线程名称
 - %(process)d: 打印进程ID
 - %(message)s: 打印日志信息
 
### 参考：
 - http://www.tuicool.com/articles/IV3meeE
