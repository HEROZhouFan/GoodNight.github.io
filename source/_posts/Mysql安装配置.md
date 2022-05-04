---
title: Mysql安装配置
date: 2022-05-01 16:13:47
tags:
  - 环境搭建
  - 软件安装
  - Mysql
categories: Mysql
---

## 下载

官网地址：https://www.mysql.com/

![image-20220501162741549](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205012741UcW8dm.png)

选择DOWNLOADS，拉到最下方

![image-20220501162805608](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205012805I12v1K.png)

![image-20220501162828867](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205012828M11Qyp.png)

![image-20220501162947485](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205012947PCz4TP.png)

![image-20220501163013025](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205013013hqoH3q.png)

---

## 安装

启动安装程序，选择第二个

![image-20220501163253971](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205013254Bt7qao.png)

输入密码

![image-20220501162246627](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022050122465Gj1FO.png)

安装完成，在系统偏好设置中找到mysql

![image-20220501162425377](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205012425HpjoKs.png)

---

## 配置环境变量

### 配置到 `~/.zshrc`文件中（重启有效）

```bash
vim ~/.zshrc
```

将mysql的`bin`目录配置到文件中

```tex
export PATH=$PATH:/usr/local/mysql/bin
```

### 配置到 `~/.bash_profile`文件中（重启后需要重新加载）

```bash
vim ~/.bash_profile
```

将`bin`目录配置到文件中后，运行下方命令加载配置

```bash
source ~/.bash_profile
```

或者将这行命令加到`~/.zshrc`文件中，开机后就会自动加载配置文件
