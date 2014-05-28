---
title: Cocos2dx 3.0 xcode5.1 竖屏
date: '2014-05-28'
description:
categories:
- cocos2dx
- xcode5
tags:
- cocos2dx
- xcode5
---

1、设置cocos2dx竖屏：

　　RootViewController.mm 中

	- (BOOL) shouldAutorotate {
	    return NO;
	}

　
	改为

	- (BOOL) shouldAutorotate {
	    return YES;
	}

2、项目竖屏

　　设置项目Targe中的Deployment Info 中的Device Orientation只勾选Portrait