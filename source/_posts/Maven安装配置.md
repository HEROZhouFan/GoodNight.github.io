---
title: Maven安装配置
date: 2022-05-04 20:57:44
tags:
  - 环境搭建
  - 软件安装
  - Maven
categories: Maven
---

## 安装

官网地址：https://maven.apache.org/

![image-20220504212547456](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220504212547EO0mql.png)

## 配置

### 配置环境变量

配置到`~/.zshrc`文件中

```bash
vim ~/.zshrc
```

将bin目录添加进去（注意这里M2_HOME换成自己的目录）

```tex
export M2_HOME=$PATH:/Users/zhoufan/devTools/apache-maven-3.8.5
export PATH=$PATH:$M2_HOME/bin
```

`Esc :wq!`保存退出

验证

```bash
mvn -v
```

### 配置`settings.xml`

打开 `/apache-maven-3.8.5/conf/settings.xml` 文件

#### 设置本地仓库位置

（没有设置的话，默认是在`${user.home}/.m2/repository`）

```tex
<localRepository>/Users/zhoufan/devTools/local_maven</localRepository>
```

#### 添加阿里云镜像

找到`</mirrors>`节点，添加

```tex
    <mirror>
      <id>nexus-aliyun</id>
      <mirrorOf>*</mirrorOf>
      <name>Nexus aliyun</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
    </mirror>
```
