---
title: QMK配置
description: 键盘开发文档
hide:
    - navigation
---

[QMK官方手册](https://docs.qmk.fm/newbs_getting_started)，使用平台 <ins>**WSL | Ubuntu 22.04 LTS**</ins>

## 1. 安装前置依赖

```shell
$ sudo apt install -y git python3-pip
```

## 2. 安装QMK主程序

```shell
$ python3 -m pip install --user qmk
```

## 3. 激活QMK

```shell
$ echo 'PATH="$HOME/.local/bin:$PATH"' >> $HOME/.bashrc
$ source $HOME/.bashrc
```

## 4. 拉取源码和后置依赖

```shell
$ qmk setup -y
```
## 5. 测试编译

```shell
$ make matrix/noah:default
```
> 编译成功后会生成`.build`文件夹，`.hex`、`.bin`或`.uf2`格式的固件

> `.hex`、`.bin`固件可使用[QMK Toolbox](https://qmk.fm/toolbox)工具烧录，`.uf2`固件直接粘贴到存储器里即可完成自动烧录
