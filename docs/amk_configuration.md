---
title: AMK配置
description: 键盘开发文档
hide:
  - navigation
---

# [AMK](https://github.com/yulei/amk)本地编译环境配置

拉取项目源码，然后编译：

```shell
$ git clone https://github.com/yulei/amk.git
$ cd amk
$ git branch checkout qmk
$ git submodule update --init --recursive
$ make onekey
```

查看可以编译的键盘固件：

```shell
$ make
```
