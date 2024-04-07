---
title: Ubuntu 22 安装 MongoDB 4
date: 2023-12-05
summary: 解决MongoDB4在Ubuntu22不可用的问题
---
**文章内容摘自[如何在 4.4 上安装 MongoDB 22.04 |APMB系列](https://www.apmb.co.uk/posts/mongodb-4.4-ubuntu-22-04/)**

（可选）首先更新软件包列表：
```shell
sudo apt update
```

复制以下全部命令以直接起飞：
```shell
echo "deb http://security.ubuntu.com/ubuntu focal-security main" | sudo tee /etc/apt/sources.list.d/focal-security.list && \
sudo apt update && \
sudo apt-get install libssl1.1 && \
sudo rm /etc/apt/sources.list.d/focal-security.list
```

然后跟着官网文档走：
[Install MongoDB Community Edition on Ubuntu — MongoDB Manual](https://www.mongodb.com/docs/v4.4/tutorial/install-mongodb-on-ubuntu/)