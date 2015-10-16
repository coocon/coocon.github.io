---
layout: post
title:  "使用charles查看https请求"
date:   2015-09-30 18:54:18
categories: other
---

####关于[charles](http://www.charlesproxy.com/):
>http的调试工具有好多：Fiddler、HttpWatch、Charles。windows上的Fiddler非常好用，不过由于需要.net的环境，在Mac上使用起来就不方便。HttpWatch 只能集成到浏览器上也不支持Mac。Charles是基于Java的,跨平台性良好，功能也强大，今天就说说charles吧。好了废话不多讲了，http的调试方法就是直接设置客户端代理服务器为Charles的ip和端口，就不细说了，现在开始说https的调试方法。

https是以安全为目标的http通道，基于SSL/TLS协议来实现。关于SSL/TLS协议，请参考阮老师的这篇文章[SSL/TLS协议运行机制的概述](http://www.ruanyifeng.com/blog/2014/02/ssl_tls.html)。
https传输的内容最后经过对称加密来和服务端进行通信,但是我们不知道密码，因此不能像普通的http随意查看。为了查看加密前的内容，我们只能获取密码才能解密。那么如何获取这个对称加密的密码呢？根据SSL/TLS协议，我们发现，如果我们冒充服务器，给浏览器我们自己的证书，那么浏览器加密以后的内容我们就可以获取到，然后拿到内容以后把自己当做client，去向真正的server发送请求，来获取真正的内容，再转发给client。代理服务器就是这个实现逻辑。关于中间人的介绍可以参考这篇文章——[解析中间人攻击之四——SSL欺骗](http://security.ctocio.com.cn/297/9483797.shtml)。







