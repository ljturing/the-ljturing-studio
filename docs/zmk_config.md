---
title: ZMK配置
description: 键盘开发文档
hide:
    - navigation
---

平台使用 <ins>**WSL | Ubuntu 22.04 LTS**</ins>，需提前**下载SDK**

- [ZMK本地配置官网](https://zmk.dev/docs/development/local-toolchain/setup/native)
- [Zephyr本地配置官网](https://docs.zephyrproject.org/latest/develop/getting_started/index.html)
- [SDK(0.16.3)](https://github.com/zephyrproject-rtos/sdk-ng/releases/tag/v0.16.3)

## 1. 安装前置依赖

CMake版本`3.20.5`，Python版本`3.10`，DTC版本`1.4.6`

```shell
$ sudo apt install -y --no-install-recommends git cmake ninja-build gperf ccache dfu-util device-tree-compiler wget python3-dev python3-pip python3-setuptools python3-tk python3-wheel xz-utils file make gcc gcc-multilib g++-multilib libsdl2-dev libmagic1
```

## 2. 拉取ZMK仓库

手动把SDK复制到ZMK项目文件夹根目录

```shell
$ git clone --recursive https://github.com/zmkfirmware/zmk.git
$ cd zmk
```

## 3. 安装west

west版本`1.3.0`；protobuf和grpcio-tools是为[ZMK studio](https://zmk.dev/docs/features/studio)准备

```shell
$ pip install west protobuf grpcio-tools
```

## 4. 初始化west

```shell
$ west init -l app/
$ west update
```

## 5. 安装后置依赖

```shell
$ west zephyr-export
$ pip install -r zephyr/scripts/requirements-base.txt
```

## 6. 安装SDK

```shell
$ tar xvf zephyr-sdk-0.16.3_linux-x86_64.tar.xz
$ ./zephyr-sdk-0.16.3/setup.sh
$ sudo cp zephyr-sdk-0.16.3/sysroots/x86_64-pokysdk-linux/usr/share/openocd/contrib/60-openocd.rules /etc/udev/rules.d
$ sudo udevadm control --reload
```

## 7. 测试编译

```shell
$ cd app
$ west build -p always -d build/corne/left -b nrfmicro_13 -- -DSHIELD=corne_left
```

编译完成后会在`build/corne/left/zephyr`文件夹下生成`.hex`、`.bin`和`.uf2`的固件

