abbrlink: 1
tags:
  - Fuchsia
categories: []
author: HanFei
title: 初识Fuchsia
date: 2018-05-06 13:24:00
---
#### 1.取代码
##### 1.1.代码
 代码位置

	官方https://fuchsia.googlesource.com/
    curl -s "https://fuchsia.googlesource.com/scripts/+/master/bootstrap?format=TEXT" | base64 --decode | bash -s <layer>

不能科学上网的，可以使用github的镜像。
	https://github.com/fuchsia-mirror
    

##### 1.2.说明
layer有如下几个可选项，使用Topaz会包含所有的layer：

	Zircon Garnet Peridot Topaz
* Zircon 微内核
* Garnet 软件管理等系统级服务
* Peridot Peridot提供所需的服务，以创建由模块、情节、代理、实体和其他组件组成的汇聚可定制的多设备用户体验。
* Topaz  通过实现底层定义的接口来增强系统功能。Topaz包含四个主要类别的软件：module，agent，shell和runner。

#### 2.Fuchsia一些技术
* jiri编译及管理git仓库
* 微内核Zircon
* 新的进程间通信接口描述方式FIDL
* 进程沙箱
* NameSpaces(文件管理与服务发现)
* Story (root application的逻辑容器)

#### 3.开源的UI开发环境Flutter
##### 3.1官网
	https://flutter.io/
##### 3.2 黑科技
* 支持导出 Android iOS 和 Fuchsia 三个平台的安装包
* Hot Reload (修改UI后，无需重新启动程序)
* 

##### 3.3 Flutter架构
![架构图](/flutter.png "Flutter")