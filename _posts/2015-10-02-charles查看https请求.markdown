---
layout: post
title:  "使用charles查看https请求"
date:   2015-09-30 18:54:18
categories: other
---

####关于[charles](http://www.charlesproxy.com/):
>http的调试工具有好多：Fiddler、HttpWatch、Charles。windows上的Fiddler非常好用，不过由于需要.net的环境，在Mac上使用起来就不方便。HttpWatch 只能集成到浏览器上也不支持Mac。Charles是基于Java的,跨平台性良好，功能也强大，今天就说说charles吧。好了废话不多讲了，http的调试方法就是直接设置客户端代理服务器为Charles的ip和端口，就不细说了，现在开始说https的调试方法。

https是以安全为目标的http通道，基于SSL/TLS协议来实现。关于SSL/TLS协议，请参考阮老师的这篇文章[SSL/TLS协议运行机制的概述](http://www.ruanyifeng.com/blog/2014/02/ssl_tls.html)。




1。新建一个没有用的改动。来测试一下。。。。。。。。


