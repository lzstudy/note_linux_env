# 常用配置

## 1 添加环境变量

- 仅对当前终端生效

```shell
export PATH=$PATH:命令行路径
```

- 仅对当前用户生效，通过修改.bashrc文件，在文件中添加如下内容。

```shell
export PATH=$PATH:命令行路径

# 添加完毕执行
source ~/.bashrc
```

- 所有用户生效，通过修改/etc/profile，

```shell
export PATH=$PATH:命令行路径

# 添加完毕执行
source /etc/profile
```

- 所有用户生效，通过修改/etc/environment文件

```shell
PATH="/usr/local/sbin:/usr/sbin:/usr/bin:/sbin:/bin"中加入":命令行路径"

# 添加完毕后重启系统
```


