---
title: Archlinux jdk7环境配置
date: '2014-05-28'
description:
categories:
- jdk配置
tags:
- archlinux
- jdk
---

一、[下载jdk](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

二、解压 并且移动|复制到/usr/lib/jvm下

三、在控制台输入　　
	
	#kate /etc/profile.d/java.sh

四、编辑java.sh

	#set java environment
	export JAVA_HOME=/usr/lib/jvm/jdk1.7.0_45  #根据实际情况创建
	export JRE_HOME=/usr/lib/jvm/jdk1.7.0_45/jre
	export CLASSPATH=.:$JAVA_HOME/lib:$JAVA_HOME/jre/lib
	export PATH=$JAVA_HOME/bin:$JRE_HOME/bin:$PATH
