imx8mp
==========

1 ISP配置
-------------

    为了独立编译ISP模块, 需要获取正确得toolchain, linux kernel, imx-isp, vvcam, 
    isp校准文件*.xml, dew校准文件*.json, 配置文件Sensor0_Entry.cfg

.. code-block:: c

    # start_isp.sh
    # 1 卸载所有模块
    rmmod imx8_media_dev + vvcam_video + vvcam_isp + vvcamdwe + imx577

    # 2 安装驱动模块
    insmod vvcam-video + imx577 + vvcam-dew + vvcam-isp + imx8-media-dev

    # 3 ./run.sh -c imx577_4K

2 网卡配置
-------------

.. code-block:: c

    # 打开配置文件
    vi /etc/systemd/network/10-eth.network

    # 进行如下修改
    [Match]
    Name=eth0
    KernelCommandLine=!root=/dev/nfs
    [Network]
    Address=192.168.0.232/24
    Gateway=192.168.0.1
    DNS=192.168.0.1


.. note:: 
    
    如果想要自动获取IP, 将 ``/etc/systemd/network/10-eth.network`` 删除即可