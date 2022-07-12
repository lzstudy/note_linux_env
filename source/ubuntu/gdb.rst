============
GDB + VSCODE
============

参考配置
--------

=============== ===================================================================================
vscode-gdb配置_ vscode配置
vscode-gdb模板_ vscode模板
=============== ===================================================================================


配置软件环境
------------

- 添加vscode gdb配置
    下载 vscode-gdb配置_ 到源码根目录下后解压.

- 配置launch.json

.. image:: .images/vscode_launch_json.jpg

- 推送gdbserver到开发板/usr/bin目录下(下表列出常用的arm-linux-gcc官网)

========== ========================================================================================
Linaro-gcc https://releases.linaro.org/components/toolchain/binaries
========== ========================================================================================


运行调试
--------

- 开发板端

::
   
   # IP地址填PC端的(非wsl ip地址)
   gdbserver 169.254.216.21:2121 main

- PC端
    打开vscode输入F5即可进入调试

.. note::

   运行前要保证板子和PC相互能ping通

.. _vscode-gdb配置: http://120.48.82.24:9100/note_linux_env/tools/vscode.tar.gz
.. _vscode-gdb模板: http://120.48.82.24:9100/note_linux_env/tools/gdb_sample.tar.gz
