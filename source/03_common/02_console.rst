终端相关
=========

1 查看控制台使用的那个终端
---------------------------

.. code-block:: shell

    $ cat /proc/device-tree/chosen/bootargs
    console=ttymxc1,115200 root=/dev/mmcblk2p2 rootwait rw

2 终端不显示工作路径
--------------------

.. code:: shell

   # 嵌入式平台vi /etc/profile
   PS1='\h:\w\$ '

3 ls彩色模式
-------------------------------

.. code:: shell

   # 嵌入式平台为/etc/profile
   # vi [/etc/profile] 或 [~/.bashrc]
   alias ls='ls --color=auto'




