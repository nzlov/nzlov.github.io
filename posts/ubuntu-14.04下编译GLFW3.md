---
title: ubuntu 14.04下编译GLFW3
date: '2014-05-28'
description:
categories:
- ubuntu
- golang
- opengl
tags:
- golang
- ubuntu
---

1、安装cmake cmake－gui

	sudo apt-get install cmake cmake-gui

　　2、使用cmake生成Makefile

	打开cmake gui，选择glfw3根目录，设置生成目录，然后点击“Configure”生成配置然后勾选“BUILD_SHARED_LIBS”，并修改“CMAKE_INSTALL_PREFIX”为“/usr”。再次点击“Configure”，然后点“Generate”。

　　3、make，make install

	使用terminal进入Makefile的生成目录，执行 “make” ，完成后再执行“sudo make install”完成安装。

 　 4、

	go get -u github.com/go-gl/glfw3

　　注意：

	如果报错 “The RandR library and headers were not found”则需要在terminal里执行“sudo apt-get install libxrandr-dev”

	如果报错 “The XInput library and headers were not found”则需要在terminal里执行“sudo apt-get install libxi-dev”