---
title: cocos2d-html5使用Ant混淆压缩
date: '2014-05-28'
description:
categories:
- cocos2d
tags:
- cocos2d
- js

---

1、下载Apache Ant

2、配置Ant环境

　　ANT_HOME

　　PATH=%PATH%;%ANT_HOME%\bin

3、使用命令行界面，运行ant -version查看时候配置好

　　![](http://images.cnitblog.com/blog/465204/201312/12213221-ddfb40e5c775479cb838e8abcb83ee7f.jpg)

4、切换到cocos2d-html5项目目录下

　　![](http://images.cnitblog.com/blog/465204/201312/12213329-c8ab999933f34928ab921132b4d0feca.jpg)

5、执行ant

　　![](http://images.cnitblog.com/blog/465204/201312/12213425-c7b0e759f1a941fca2475d864aedf7da.jpg)

6、编辑cocos2d.js文件

　　![](http://images.cnitblog.com/blog/465204/201312/12213634-e488251a377a4c06b202157b1745e074.jpg)
	
	将 engineDir:'../cocos2d/' 以及 appFiles:[] 这两段注释掉，将 SingleEngineFile 取消注释并编辑后面的值为打包后的值。

7、成功！