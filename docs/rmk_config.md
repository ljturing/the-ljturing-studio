---
title: RMK配置
description: 键盘开发文档
hide:
    - navigation
---

[Rust官方手册](https://doc.rust-lang.org/book/ch01-01-installation.html)，平台使用 <ins>**WSL | Ubuntu 22.04 LTS**</ins>

## 1. 安装前置依赖

```shell
$ sudo apt install -y curl git python3 libssl-dev pkg-config
```

## 2. 安装Rust

```shell
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
$ . "$HOME/.cargo/env"
```

## 3. 安装工具链

这里是nRF52840，其他工具链安装参考[这里](https://docs.rust-embedded.org/book/intro/install.html#rust-toolchain)

```shell
$ rustup target add thumbv7em-none-eabihf
```

## 4. 安装后置依赖

```shell
$ cargo install rmkit flip-link cargo-make
$ source $HOME/.cargo/env
```

## 5. 拉取源码

```shell
$ git clone --recursive https://github.com/HaoboGu/rmk.git
```

## 6. 编译测试

```shell
$ cd rmk/examples/use_rust/nrf52840
$ cargo make -r
```

编译通过后会在`build`文件夹下直接生成`.uf2`固件文件，由于主控是使用nRF52840，所以直接使用`cargo make`生成`.uf2`固件；如果需要`.hex`或者`.bin`固件，使用`cargo build -r`即可

