---
title: proxy 代理命令格式
date: 2023-04-09T12:20:00.000Z
summary: 注：本教程不可以直接复制粘贴，只是命令格式的速记，请按照**实际情况**使用
---

注：本教程不可以直接复制粘贴，只是命令格式的速记，请按照**实际情况**使用

```shell
$proxy_url == http://<username>:<password>@<proxy_host>:<port>
```

# 通用

## linux 环境变量

```shell
export http_proxy/https_proxy/socket_proxy/HTTP_PROXY/HTTPS_PROXY='$proxy_url'
```

## git 代理命令

```shell
git config --global http.proxy $proxy_url
git config --global https.proxy $proxy_url
```

## pip 代理命令

```shell
pip config set global.proxy $proxy_url
```

## conda 代理命令

```shell
conda config --set proxy_servers.http $proxy_url
conda config --set proxy_servers.https $proxy_url
```
