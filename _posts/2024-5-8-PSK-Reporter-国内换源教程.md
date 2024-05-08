---
layout: post
title: PSK Reporter 国内换源教程
---
[PSK Reporter](https://www.pskreporter.info/)是一款业余无线电常用的信号报告系统。全世界的业余无线电爱好者们可以将自己收到的各种数字信号（甚至不止数字信号，SSB、SSTV信号也可以）上传至这个网站上，其他爱好者就可以知道他们的信号是否被别人接收到，从而检查他们的电台发射设备是否正常，以及信号传播情况的好坏。
然而，PSK Reporter在中国大陆的网络访问却加载不出来功能。其原因无非就是PSK Reporter使用了一些墙内不能访问的资源。经过检查后，PSK Reporter分别使用了Google的一系列服务资源，以及[bootstrapcdn.com](https://www.bootstrapcdn.com/)的前端工具包资源，这两个资源无法在墙内访问到。解决这个问题最快的方法其实就是使用科学上网的手段，以下方法适用于没有科学上网手段的同学。
### Google服务
Google服务在很多网站上都有使用，包括[QRZ.com](https://www.qrz.com/)的电子日志。由于Google服务被墙，所以原本其他内容可以正常访问的网站也无法访问。这个问题的解决方法可以参考这篇B站视频[【业余无线电】QRZ Logbook页面白屏？让我助你一臂之力！](https://www.bilibili.com/video/BV1NZ4y1j7e8)。这篇视频使用了Chrome系或者火狐浏览器的插件替换了Google的服务源，这样在国内便可访问替代的源，也可以实现相同功能。
### Bootstrap CDN
解决了Google CDN的问题之后，访问PSK Reporter，发现还是不能正常打开。切换到控制台查看报错，发现有一个bootstrap.min.css的前端文件没加载出来。鼠标移动到报错信息上面，提示网页使用了[https://stackpath.bootstrapcdn.com/](https://stackpath.bootstrapcdn.com/)的源。Ping一下，果然ping不通，看样子这个网站也被墙了。
![PSK](/pictures/psk_not_succeed.png)
从报错信息看，PSK Reporter使用了4.1.1版本的Bootstrap CDN。在网上搜了一下，发现了一个可用的CDN [Bootstrap 4.1.1 CDN - UseBootstrap](https://usebootstrap.com/cdn/4.1.1)。于是在hosts文件里面将stackpath.bootstrapcdn.com替换成上面页面提示的cdn.usebootstrap.com。（有关hosts是干什么的，可参考[如何修改hosts文件？几种修改hosts文件的方法 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/438447914)）
![ping](/pictures/ping.png)
结果发现替换后bootstrap.min.css还是加载不出来。尝试ping了一下，结果发现cdn.usebootstrap.com的域名在国内疑似被替换成了一个IPv6地址，看样子应该还是域名被改到其他地方了。使用查询IP的网站（比如[IPv4 网站测速 | IP查询(ipw.cn)](https://ipw.cn/speedtest/)）查询了一下cdn.usebootstrap.com的原始IPv4地址，替换至hosts中，保存，成功进入PSK Reporter。
![hosts](/pictures/hosts.png)
