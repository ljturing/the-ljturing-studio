---
title: 其他
description: 键盘开发文档
hide:
    - navigation
---

## 一些使用Linux的常规操作

```shell
# 安装UF2转换工具
python3 -m pip install --pre -U git+https://github.com/makerdiary/uf2utils.git@main

# .elf转.hex
objcopy -O ihex *.elf *.hex

# .elf转.bin
objcopy -O binary *.elf *.bin

# .hex转.uf2
uf2conv -f 0xADA52840 -c -o *.uf2 *.hex

# .bin转.uf2
uf2conv -f 0xADA52840 -c -b 0x1000 -o *.uf2 *.bin

# 查找.Identifier文件并删除
find . -name "*.Identifier" -exec rm -rf {} \;

# 安装Scoop/python/mkdocs，在PowerShell输入
$ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
$ Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
$ scoop install python
$ python3 -m pip install --upgrade pip
$ pip install mkdocs mkdocs-material
```
