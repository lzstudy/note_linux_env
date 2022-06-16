# 帅气的分类

## 推送本地公钥到服务器

```shell
cat ~/.ssh/id_rsa.pub | ssh USER@HOST "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
```

## Linux通过网页下载

```shell
wget https://gerrit-releases.storage.googleapis.com/gerrit-3.2.3.war
```

## pip install指定清华源

```shell
pip install package -i https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple/
```
