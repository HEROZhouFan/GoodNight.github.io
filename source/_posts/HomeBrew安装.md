---
title: HomeBrew安装
date: 2022-04-23 17:10:50
tags:
  - 环境搭建
  - 软件安装
  - HomeBrew
categories: HomeBrew
---

官网地址：https://brew.sh/index_zh-cn

**官网安装命令**：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

可能由于网络原因安装慢，或者是安装失败

**卸载Homebrew**（先卸载之前下载的部分文件）

```bash
ruby -e "S(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"
```

**重新安装Homebrew**（这个安装会快很多）

```bash
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```

建议选择 **中科大** 镜像源
