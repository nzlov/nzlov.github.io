---
title: Golang archlinux下环境配置
date: '2014-05-28'
description:
categories:
- golang
- archlinux
tags:
- golang
- archlinux
---

一、准备

　　1）golang

　　　　下载地址：https://code.google.com/p/go/

　　2）liteide

　　　　推荐下载源码自己编译，官方编译的可能在archlinux上因为qt更新问题出现异常。

　　　　下载地址：

	Source code ： https://github.com/visualfc/liteide

	Binary downloads ： http://code.google.com/p/golangide

　　3）git

	安装：
	
	#pacman -S git

	最好有github的帐号～并且导入ssh，现在golang的第三方库在github上。

　　4）mercurial

	安装：
	
	#pacman -S mercurial

二、配置环境

　　1）golang

　　　　archlinux中配置环境最好放到自启动中，在$HOME下会出问题。

	#kate /etc/profile.d/go.sh
	
	#set go environment
	export GOROOT=/home/nzlov/Software/go 　　#自己替换Go目录
	export GOARCH=386　　　　　　　　　　　  #根据自己电脑设置386/amd64
	export GOOS=linux
	export GOPATH=/home/nzlov/Workspaces/Go  #根据自己的Go工作目录替换
	export GOBIN=$GOPATH/bin
	export PATH=$GOBIN:$PATH
　
　2）gocode

　　　　配置好golang、git及mercurial后，打开控制台输入
	
	go get github.com/nsf/gocode

	go install github.com/nsf/gocode 

　　3）liteide

　　　　解压后使用控制台进入liteide的目录

　　　　执行：

	cd build
	./build_linux.sh

　　　　等待编译完成。

　　　　如果执行出现：error，QTDIR is null 则需要设置qt的目录 通常是 /usr/lib/qt4

　　完成！
