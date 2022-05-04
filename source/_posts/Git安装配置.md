---
title: Git安装配置
date: 2022-05-01 11:17:12
tags:
  - 环境搭建
  - 软件安装
  - HomeBrew
  - Git
  - GitHub
categories: Git
---

## 安装git

```bash
brew install git
```

查看是否安装完成

```bash
git --version
```

---

## 配置git

设置用户名

```bash
git config --global user.name "username"
```

设置邮箱

```bash
git config --global user.email "email"
```

![image-20220501115104335](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022050151048TgDsY.png)

---

## 绑定GitHub

生成密钥 SSH key

```bash
ssh-keygen -t rsa -C '上面配置的邮箱'
```

按照提示完成三次回车，即可生成 ssh key

找到生成的 .pub 文件

/Users/zhoufan/.ssh/id_rsa.pub（隐藏文件 `shift+command+.` 显示）

![image-20220501120353031](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022050103533R3c6B.png)

登录github账号，进入到`Settings`

![image-20220501120532010](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205010532qChpg2.png)

New SSH key

![image-20220501120652212](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205010652waBJ5v.png)

取一个名字，将.pub 的密钥粘贴进来

![image-20220501120830155](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205010830gF3ckR.png)

![image-20220501120846457](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205010846bXuJ3W.png)

这样就配置好了 SSH 访问 Github 的权限

最后测试一下

```bash
ssh -T git@github.com
```

输入本机密码

连接成功

![image-20220501121628848](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205011628vBDwtb.png)

---

## Sourcetree

HomeBrew cask安装Sourcetree

```bash
brew install --cask sourcetree
```

下载完成后在启动台找到

打开`偏好设置`

![image-20220501122035070](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205012035vsKFnH.png)

点击`连接账号`添加账号
