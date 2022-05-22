---
title: Git代理设置
date: 2022-05-04 21:58:21
tags:
  - Git
  - VPN
  - proxy
  - GitHub
categories: Git
---

git clone 一直报错

```bash
OpenSSL SSL_connect: Connection was reset in connection to github.com:443
```

网上找了很久发现是因为开了VPN代理的问题

## Git 设置代理

查看自己的VPN端口号，假如你的端口号是7890，在git bash命令行中输入以下命令即可：

```bash
git config --global http.proxy 127.0.0.1:7890
```

```bash
git config --global https.proxy 127.0.0.1:7890
```

如果你之前git中已经设置过上述配置，则使用如下命令取消再进行配置即可：

```bash
git config --global --unset http.proxy
```

```bash
git config --global --unset https.proxy
```

### 其他查看配置的命令

#### 查看git的所有配置

```bash
git config --global -l
```

#### 查看git的http代理配置

```bash
git config --global http.proxy
```

#### 查看git的https代理配置

```bash
git config --global https.proxy
```

## IDEA 设置代理

![image-20220504220743061](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220504220743wBi1H8.png)

**参考博客**：https://blog.csdn.net/qq_37555071/article/details/114260533
