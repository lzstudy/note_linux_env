# vscode + gdb

## 源码和源码

| 文件                                                                        | 说明                    |
| --------------------------------------------------------------------------- | ----------------------- |
| [gdb-7.3.1](http://120.48.82.24:9100/note_linux_env/tools/gdb-7.3.1.tar.gz) | gdb-7.3.1源码           |
| [gdbserver](http://120.48.82.24:9100/note_linux_env/tools/gdbserver-mt7621) | gdbserver用于mt7621平台 |


## 环境说明

- wsl + ubuntu18.04

- mips交叉编译路径 /opt/mips-openwrt-mt7621


## 配置源码

- 进入gdbserver目录

```shell
tar -vxf gdb-7.3.1.tar.gz
cd gdb-7.3.1/gdb/gdbserver
```

- 配置编译信息

```shell
CC=/opt/mips-openwrt-mt7621/staging_dir/toolchain-mipsel_24kc_gcc-7.3.0_musl/bin/mipsel-openwrt-linux-gcc  CXX=/opt/mips-openwrt-mt7621/staging_dir/toolchain-mipsel_24kc_gcc-7.3.0_musl/bin/mipsel-openwrt-linux-g++ ./configure --target=mipsel-linux --host=mipsel-linux
```

## 修改源码

- 修改Makefile

```c
# 将警告报错的选项屏蔽掉
# WERROR_CFLAGS = -Werror              // 大概在90行左右
```

- 修改linux-low.c

>> 把出错的struct siginfo结构体 替换为siginfo_t

- 修改linux-mips-low.c

>> 把有冲突的函数全部注释掉, 168行 - 

- 修改proc-service.c

>> 把有冲突的函数全部注释掉, 136 - 153行

## 编译源码

>> 执行make命令, 执行完毕后会在当前目录下生成gdbserver文件, 使用file命令验证是否为mips架构的程序


