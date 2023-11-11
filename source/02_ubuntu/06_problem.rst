其他问题
==============

1 Windons无法复制粘贴到Ubuntu
----------------------------------

.. code-block:: c

    sudo apt-get autoremove open-vm-tools
    sudo apt-get install open-vm-tools
    sudo apt-get install open-vm-tools-desktop

2 重启wsl
---------------

.. code-block:: c

    # 在powershell以管理员方式打开
    net stop LxssManager
    net start LxssManager
