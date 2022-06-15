# WSL2环境搭建

## 一、WSL介绍

Wsl - windows subsystem for linux，可以在windows上使用linux开发，并且可以直接调用windows命令。wsl基于hyper5虚拟机（win10内置）


## 二、官方文档连接

[https://docs.microsoft.com/zh-cn/windows/wsl/install](https://docs.microsoft.com/zh-cn/windows/wsl/install)  


## 三、WSL简易安装


- 在[Microsoft Store](https://aka.ms/wslstore)获取并安装Ubuntu18

![ubuntu_install](.images/ubuntu.png)


- 在[Microsoft Store](https://aka.ms/wslstore)获取并安装Windows Terminal

![ubuntu_install](.images/terminal.png)


- 安装wsl

```PowerShell
wsl --install
```


- ws升级为wsl2，首先需要下载并安装[wsl内核升级组件](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

```PowerShell
wsl --set-default-version Ubuntu18.04 2
```

- wsl迁移，默认wsl安装C盘，为了防止爆盘，建议把wsl迁移到其他盘符。下载迁移工具[LxRunOffline-v3.5.0-mingw.zip](http://120.48.82.24:9100/note_linux_env/ubuntu/LxRunOffline-v3.5.0-mingw.zip)

```PowerShell
.\LxRunOffline.exe move -n Ubuntu-18.04 -d D:\wsl
```

- 查看是否迁移成功 

```
.\LxRunOffline.exe get-dir -n Ubuntu-18.04
```

