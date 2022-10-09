# 常见问题
## 1 Windons无法复制粘贴到Ubuntu

### 1.1 执行以下命令后，重启系统

```shell
sudo apt-get autoremove open-vm-tools
sudo apt-get install open-vm-tools
sudo apt-get install open-vm-tools-desktop
```

### 1.2 重启wsl

```shell
# 在powershell以管理员方式打开
net stop LxssManager
net start LxssManager
```
