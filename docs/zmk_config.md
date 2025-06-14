---
title: ZMK配置
description: 键盘开发文档
hide:
    - navigation
---

!!! note "注意"
    平台使用 <ins>**WSL | Ubuntu 22.04 LTS**</ins>，需提前**下载SDK**

    - [ZMK本地配置官网](https://zmk.dev/docs/development/local-toolchain/setup/native)
    - [Zephyr本地配置官网](https://docs.zephyrproject.org/latest/develop/getting_started/index.html)
    - [SDK(0.16.3)](https://github.com/zephyrproject-rtos/sdk-ng/releases/tag/v0.16.3)

## 1. 安装前置依赖

!!! tip "依赖版本要求"
    | CMake | Python | DTC |
    | :-: | :-: | :-: |
    | 3.20.5 | 3.10 | 1.4.6 |

```shell
sudo apt install -y --no-install-recommends git cmake ninja-build gperf ccache dfu-util device-tree-compiler wget python3-dev python3-pip python3-setuptools python3-tk python3-wheel xz-utils file make gcc gcc-multilib g++-multilib libsdl2-dev libmagic1
```

## 2. 拉取ZMK仓库

手动把SDK复制到ZMK项目文件夹根目录

```shell linenums="1"
git clone --recursive https://github.com/zmkfirmware/zmk.git
cd zmk
```

## 3. 安装west

!!! tip "west版本要求"
    | west |
    | :-: |
    | 1.3.0 |

    `protobuf`和`grpcio-tools`是为[ZMK studio](https://zmk.dev/docs/features/studio)准备

```shell
pip install west protobuf grpcio-tools
```

## 4. 初始化west

```shell linenums="1"
west init -l app/
west update
```

## 5. 安装后置依赖

```shell linenums="1"
west zephyr-export
pip install -r zephyr/scripts/requirements-base.txt
```

## 6. 安装SDK

```shell linenums="1"
tar xvf zephyr-sdk-0.16.3_linux-x86_64.tar.xz
./zephyr-sdk-0.16.3/setup.sh
sudo cp zephyr-sdk-0.16.3/sysroots/x86_64-pokysdk-linux/usr/share/openocd/contrib/60-openocd.rules /etc/udev/rules.d
sudo udevadm control --reload
```

## 7. 测试编译

```shell linenums="1"
cd app
west build -p always -d build/corne/left -b nrfmicro_13 -- -DSHIELD=corne_left
```

!!! success "验证"
    编译完成后会在`build/corne/left/zephyr`文件夹下生成`zephyr.hex`、`zephyr.bin`和`zephyr.uf2`的固件

