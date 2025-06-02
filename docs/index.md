---
title: 主页
description: 键盘开发文档
hide:
  - navigation
---

## 🚀已完成开发的键盘套件

| 套件 | VID | PID | 特性 | 验证 |
| :-: | :-: | :-: | :-: | :-: |
| Palice | 0x5123 | 0xA001 | 32U4/F103, Alice | ✅ |
| Luolin | 0x5123 | 0xA002 | 16U2 | 🚧 |
| AD43 R1 | 0x5123 | 0xA003 | 32U4 | 🚧 |
| AD43 R2 | 0x5123 | 0xA004 | F103, RGB | ✅ |
| Carve80 V2 | 0x5123 | 0xA005 | F103, RGB | ✅ |
| Hl75 | 0x5123 | 0xA006 | F103, RGB | ✅ |
| Link65 | 0x5123 | 0xA007 | F103, HC595 | ✅ |
| Ghost65 | 0x5123 | 0xA008 | F103 | ✅ |
| KBD65 | 0x5123 | 0xA009 | F103 | ✅ |
| DoysPad | 0x5123 | 0xA00B | F401, nRF52810, RGB | ✅ |
| Feather | 0x5123 | 0xA00C | 32U4, nRF51822 | ✅ |
| China64 | 0x5123 | 0xA00D | F103 | ✅ |
| China65 | 0x5123 | 0xA00E | F103 | ✅ |
| China21BLE | 0x5123 | 0xA00F | 32U4, nRF51822 | 🚧 |
| Changer | 0x5123 | 0xA010 | F072 | ✅ |
| Loli80 | 0x5123 | 0xA011 | F103 | ✅ |
| Zhaolele | 0x5123 | 0xA012 | F103 | ✅ |
| Corne44 | 0x5123 | 0xA013 | RP2040，RGB，分体，SSD1306，旋钮，摇杆 | ✅ |
| JPad22 | 0x5123 | 0xA014 | 32U4，RGB，SSD1306，旋钮 | ✅ |
| Artsey8 | 0x5123 | 0xA015 | RP2040 | ✅ |
| Yb590 | 0x5123 | 0xA016 | 32U4，RGB，旋钮 | ✅ |
| Prometheus | 0x5123 | 0xA017 | F411，RGB | ✅ |
| SillShawn2024P | 0x5123 | 0xA018 | F401 | ✅ |
| Lily43 | 0x5123 | 0xA019 | F401，RGB | ✅ |
| HHKB60 | 0x5123 | 0xA01A | F103 | ✅ |
| Peculiar119 | 0x5123 | 0xA01B | F103 | ✅ |
| Woody89 | 0x5123 | 0xA01C | 32U4 | ✅ |
| NK17 | 0x5123 | 0xA01D | F103 | ✅ |
| Puu48 | 0x5123 | 0xA01E | RP2040 | ✅ |
| Vintage4_x | 0x5123 | 0xA01F | F103 | ✅ |
| GH6X | 0x5123 | 0xA020 | F103 | ✅ |
| LaunchPad78 | 0x5123 | 0xA021 | F103 | ✅ |
| CYKB102 | 0x5123 | 0xA022 | F103 | ✅ |
| MK23S | 0x5123 | 0xA023 | F401 | ✅ |
| QVIA35L | 0x5123 | 0xA024 | F401，WCH582，RGB，摇杆 | ✅ |
| QVIA35R | 0x5123 | 0xA025 | F401，WCH582，RGB，摇杆 | ✅ |
| MK71 | 0x5123 | 0xA027 | F411，RGB，旋钮，SSD1306，分体 | ✅ |
| Mojo17 | 0x5123 | 0xA028 | F411，WCH582，RGB | ✅ |
| QVIA66 | 0x5123 | 0xA029 | F401，WCH582，RGB，摇杆 | ✅ |
| Mr.Lu | 0x5123 | 0xA02A | F103，RGB | ✅ |


## 🚀一些开源键盘固件对比

| | [AMK](https://github.com/yulei/amk) | [KMK](https://github.com/KMKfw/kmk_firmware) | [QMK](https://github.com/qmk/qmk_firmware) | [RMK](https://github.com/HaoboGu/rmk) | [ZMK](https://github.com/zmkfirmware/zmk) |
| :- | :-: | :-: | :-: | :-: | :-: |
| 语言 | C | Python | C | Rust | C |
| USB | ✅ | ✅ | ✅ | ✅ | ✅ |
| 蓝牙 | ✅ | ✅ | | ✅ | ✅ |
| 实时编辑键映射 | ✅ | ✅ | ✅ | ✅ | 🚧 |
| 有线分体 | ✅ | | ✅ | 🚧 | |
| 无线分体 | | ✅ | | ✅ | ✅ |
| ARM芯片（STM32/nRF/RP2040） | ✅ | ✅ | ✅ | ✅ | ✅ |
| RISC-V和Xtensa芯片 | | | | ✅ | |
| 鼠标键 | ✅ | ✅ | ✅ | ✅ | 🚧 |
| 配置 | json + makefile | micropython | json + makefile | toml | Kconfig + devicetree |
| 层/宏/媒体键 | ✅ | ✅ | ✅ | ✅ | ✅ |



一些主流开源键盘固件的本地配置文档，都是对官方文档进行精简，不适合新手。遇到任何问题请查看官方文档或联系我。

- [AMK配置](./amk_configuration.md)

- [KMK配置](./kmk_configuration.md)

- [QMK配置](./qmk_configuration.md)

- [RMK配置](./rmk_configuration.md)

- [ZMK配置](./zmk_configuration.md)
