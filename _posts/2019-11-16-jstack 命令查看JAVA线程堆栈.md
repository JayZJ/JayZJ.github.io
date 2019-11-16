---
layout:     post
title:      jstack 命令查看JAVA线程堆栈
subtitle:   Jdk、Thread、Java
date:       2019-11-16
author:     HJ
header-img: img/post-bg-debug.png
catalog: true
tags:
    - Java
---


>jstack 命令。

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [JAVA堆栈信息](#java%E5%A0%86%E6%A0%88%E4%BF%A1%E6%81%AF)
- [jps -lvm](#jps--lvm)
- [jstack -l pid](#jstack--l-pid)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

### JAVA堆栈信息
实际生产中，可能由于开发以及测试未能全面覆盖的代码质量、性能问题，而引致线程挂起甚至崩溃。可能就需要查看堆栈信息来排查问题了。
### jps -lvm
jps -lvm 用于查看当前机器上运行的java进程。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191116104338169.png)
我们看到当前计算机运行了3个java进程，进程id为267064的是我们的应用服务，我们需要查看其堆栈信息。

### jstack -l pid
![在这里插入图片描述](https://img-blog.csdnimg.cn/2019111610454680.png)
