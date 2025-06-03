---
title: AMK配置
description: 键盘开发文档
hide:
    - navigation
---

!!! note "注意"
    使用平台 <ins>**WSL | Ubuntu 22.04 LTS**</ins>

## 1. 拉取项目源码

```shell linenums="1"
git clone https://github.com/yulei/amk.git
cd amk
git branch checkout qmk
git submodule update --init --recursive
```
## 2. 编译

```shell
make onekey
```

!!! tip "提示"
    使用`make`可以查看可编译的键盘固件

