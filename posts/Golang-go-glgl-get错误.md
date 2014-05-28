---
title: Golang go-glgl get错误
date: '2014-05-28'
description:
categories:
- golang
- gogl
tags:
- golang
- gogl
---

由于gl使用了cgo，所以需要配置环境MinGW.

gl需要glew支持，所以从官网下载glew-win，但是没有这个包内没有提供mingw使用.a文件。

于是下载glew的源码.tar，先用MinGW make。

然后再go get github.com/go-gl/gl