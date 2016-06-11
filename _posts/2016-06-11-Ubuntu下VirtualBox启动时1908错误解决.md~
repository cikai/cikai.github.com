---
layout: post
title:  "Ubuntu下VirtualBox启动时1908错误解决"
date:   2016-06-11 17:23:36 +0800
categories: jekyll update
---
笔记本是Ubuntu系统，刚才用VirtualBox启动Windows7时，无法启动。

#### 错误信息

	Kernel driver not installed (rc=-1908)

	The VirtualBox Linux kernel driver (vboxdrv) is either not loaded or there is a permission problem with
	/dev/vboxdrv. Re-setup the kernel module by executing

	'/etc/init.d/vboxdrv setup'

	as root. Users of Ubuntu, Fedora or Mandriva should install the DKMS package first.
	This package keeps track of Linux kernel changes and recompiles the vboxdrv kernel module if necessary.

### 解决方法-1(自己机器)

#### 1. 确认系统是否安装了gcc

	sudo apt-get install gcc

#### 2. 执行以下命令

	sudo /etc/init.d/vboxdrv setup

待程序重新编译后，可以正常运行。

### 解决方法-2（网上传的）

执行以下命令：

	sudo aptitude update

	sudo aptitude install dkms

	sudo /etc/init.d/vboxdrv setup

### 总结

出现Kernel driver not installed (rc=-1908)错误的原因是，没有编译成功供virtualbox使用的内核模块，要编译出这个模块，需要内核源代码；其次是需要编译器，linux下就是gcc，这两个都满足了，再执行

	sudo /etc/init.d/vboxdrv setup


