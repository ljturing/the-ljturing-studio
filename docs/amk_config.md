---
title: AMK配置
description: 键盘开发文档
hide:
    - navigation
---

## 1. 拉取项目源码

```shell
$ git clone https://github.com/yulei/amk.git
$ cd amk
$ git branch checkout qmk
$ git submodule update --init --recursive
```
## 2. 编译

```shell
$ make onekey
```

## 查看可以编译的键盘固件

```shell
$ make
```
