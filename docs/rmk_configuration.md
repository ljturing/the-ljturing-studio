---
title: RMK配置
description: 键盘开发文档
hide:
  - navigation
---

# [RMK](https://haobogu.github.io/rmk/index.html)本地编译环境配置

[Rust官方手册](https://doc.rust-lang.org/book/ch01-01-installation.html)，平台使用 <ins>**WSL | Ubuntu 22.04 LTS**</ins>

安装依赖

```shell
$ sudo apt-get update
$ sudo apt-get upgrade -y
$ sudo apt install -y curl git python3 libssl-dev pkg-config
```

安装Rust

```shell
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
$ . "$HOME/.cargo/env"
```

安装工具链，这里是nRF52840

```shell
$ rustup target add thumbv7em-none-eabihf
```

安装其他依赖

```shell
$ cargo install rmkit flip-link cargo-make
$ source $HOME/.cargo/env
```
