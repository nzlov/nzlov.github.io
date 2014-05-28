---
title: Go GUI不显示控制台
date: '2014-05-28'
description:
categories:
- golang
tags:
- golang

---

构建时加入参数
	 -ldflags "-H windowsgui"

	eg：go build -ldflags "-H windowsgui" project.go
