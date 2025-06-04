---
title: 主页
description: 键盘开发文档
hide:
    - navigation
    - toc
---

## 🚀已完成开发的键盘套件

| | 套件 | VID | PID | 特性 | 验证 |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 1 | Palice | 0x5123 | 0xA001 | 32U4/F103，Alice | ✅ |
| 2 | Luolin | 0x5123 | 0xA002 | 16U2 | 🚧 |
| 3 | AD43 R1 | 0x5123 | 0xA003 | 32U4 | 🚧 |
| 4 | AD43 R2 | 0x5123 | 0xA004 | F103，RGB | ✅ |
| 5 | Carve80 V2 | 0x5123 | 0xA005 | F103，RGB | ✅ |
| 6 | Hl75 | 0x5123 | 0xA006 | F103，RGB | ✅ |
| 7 | Link65 | 0x5123 | 0xA007 | F103，HC595 | ✅ |
| 8 | Ghost65 | 0x5123 | 0xA008 | F103 | ✅ |
| 9 | KBD65 | 0x5123 | 0xA009 | F103 | ✅ |
| 10 | DoysPad | 0x5123 | 0xA00B | F401，nRF52810, RGB | ✅ |
| 11 | Feather | 0x5123 | 0xA00C | 32U4，nRF51822 | ✅ |
| 12 | China64 | 0x5123 | 0xA00D | F103 | ✅ |
| 13 | China65 | 0x5123 | 0xA00E | F103 | ✅ |
| 14 | China21BLE | 0x5123 | 0xA00F | 32U4，nRF51822 | 🚧 |
| 15 | Changer | 0x5123 | 0xA010 | F072 | ✅ |
| 16 | Loli80 | 0x5123 | 0xA011 | F103 | ✅ |
| 17 | Zhaolele | 0x5123 | 0xA012 | F103 | ✅ |
| 18 | Corne44 | 0x5123 | 0xA013 | RP2040，RGB，分体，SSD1306，旋钮，摇杆 | ✅ |
| 19 | JPad22 | 0x5123 | 0xA014 | 32U4，RGB，SSD1306，旋钮 | ✅ |
| 20 | Artsey8 | 0x5123 | 0xA015 | RP2040 | ✅ |
| 21 | Yb590 | 0x5123 | 0xA016 | 32U4，RGB，旋钮 | ✅ |
| 22 | Prometheus | 0x5123 | 0xA017 | F411，RGB | ✅ |
| 23 | SillShawn2024P | 0x5123 | 0xA018 | F401 | ✅ |
| 24 | Lily43 | 0x5123 | 0xA019 | F401，RGB | ✅ |
| 25 | HHKB60 | 0x5123 | 0xA01A | F103 | ✅ |
| 26 | Peculiar119 | 0x5123 | 0xA01B | F103 | ✅ |
| 27 | Woody89 | 0x5123 | 0xA01C | 32U4 | ✅ |
| 28 | NK17 | 0x5123 | 0xA01D | F103 | ✅ |
| 29 | Puu48 | 0x5123 | 0xA01E | RP2040 | ✅ |
| 30 | Vintage4_x | 0x5123 | 0xA01F | F103 | ✅ |
| 31 | GH6X | 0x5123 | 0xA020 | F103 | ✅ |
| 32 | LaunchPad78 | 0x5123 | 0xA021 | F103 | ✅ |
| 33 | CYKB102 | 0x5123 | 0xA022 | F103 | ✅ |
| 34 | MK23S | 0x5123 | 0xA023 | F401 | ✅ |
| 35 | QVIA35L | 0x5123 | 0xA024 | F401，WCH582，RGB，摇杆 | ✅ |
| 36 | QVIA35R | 0x5123 | 0xA025 | F401，WCH582，RGB，摇杆 | ✅ |
| 37 | MK71 | 0x5123 | 0xA027 | F411，RGB，旋钮，SSD1306，分体 | ✅ |
| 38 | Mojo17 | 0x5123 | 0xA028 | F411，WCH582，RGB | ✅ |
| 39 | QVIA66 | 0x5123 | 0xA029 | F401，WCH582，RGB，摇杆 | ✅ |
| 40 | Mr.Lu | 0x5123 | 0xA02A | F103，RGB | ✅ |

## 🚀一些开源键盘固件对比

!!! note "注意"
    一些主流开源键盘固件的本地配置文档，都是对官方文档进行精简。遇到任何问题请查看官方文档或联系我！

    点击下方标题可跳转官方网页

| | [AMK](https://github.com/yulei/amk) | [KMK](https://github.com/KMKfw/kmk_firmware) | [QMK](https://github.com/qmk/qmk_firmware) | [RMK](https://github.com/HaoboGu/rmk) | [ZMK](https://github.com/zmkfirmware/zmk) |
| :- | :-: | :-: | :-: | :-: | :-: |
| 语言 | C | Python | C | Rust | C |
| USB | ✅ | ✅ | ✅ | ✅ | ✅ |
| 蓝牙 | ✅ | ✅ | | ✅ | ✅ |
| 实时编辑键映射 | ✅ | ✅ | ✅ | ✅ | 🚧 |
| 有线分体 | ✅ | | ✅ | 🚧 | |
| 无线分体 | | ✅ | | ✅ | ✅ |
| ARM芯片（STM32/nRF/RP2040） | ✅ | ✅ | ✅ | ✅ | ✅ |
| RISC-V和Xtensa芯片 | | | 仅支持GD32 | ✅ | |
| 鼠标键 | ✅ | ✅ | ✅ | ✅ | 🚧 |
| 配置 | json + makefile | micropython | json + makefile | toml | Kconfig + devicetree |
| 层/宏/媒体键 | ✅ | ✅ | ✅ | ✅ | ✅ |


[AMK配置](./amk_config.md){: .md-button .md-button--primary }
[KMK配置](./kmk_config.md){: .md-button .md-button--primary }
[QMK配置](./qmk_config.md){: .md-button .md-button--primary }
[RMK配置](./rmk_config.md){: .md-button .md-button--primary }
[ZMK配置](./zmk_config.md){: .md-button .md-button--primary }

