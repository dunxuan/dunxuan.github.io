---
title: Debian报错及修复方法
date: 2022-12-16T01:31:00.000Z
summary: 只存在于debian的某一个版本
---
```shell
E: The repository 'http://security.debian.org./debian-security
bullseye/updates Release' does not have a Release file.
```

Debian 报这个错是因为官方错误配置 Apt 源的问题，打开`/etc/apt/sources.list`，错误配置如下：

```shell
deb http://security.debian.org/debian-security/ bullseye/updates main
deb-src http://security.debian.org/debian-security/ bullseye/updates main
```

**修复方法按照情况选一种：**

## 更换官方源

将错误配置修改为：

```shell
deb http://security.debian.org/debian-security/ bullseye-security main
deb-src http://security.debian.org/debian-security/ bullseye-security main
```

## 更换国内源

国内机子建议使用国内源。
以**清华镜像**为例：

```shell
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye main contrib non-free
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-updates main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-updates main contrib non-free

deb https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-backports main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ bullseye-backports main contrib non-free

deb https://mirrors.tuna.tsinghua.edu.cn/debian-security bullseye-security main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian-security bullseye-security main contrib non-free
```