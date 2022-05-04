---
title: Node.js安装配置
date: 2022-05-01 12:28:17
tags:
  - 环境搭建
  - 软件安装
  - Node.js
categories: Node.js
---

## Node.js

### 安装

官网地址：https://nodejs.org/en/

官网下载安装包，傻瓜式安装

### 查看npm版本

```bash
npm -v
```

### 查看Node.js版本

```bash
node -v
```

---

## 配置镜像源

### 设置淘宝镜像源

```bash
npm config set registry https://registry.npm.taobao.org
```

### 验证

```bash
npm config get registry
```

---

## cnpm

### 安装

```bash
sudo npm install -g cnpm --registry=https://registry.npm.taobao.org
```

### cnpm下载

```bash
cnpm install express
```

---

## n -Node.js版本管理工具

### 安装

```bash
sudo npm install n -g
```

### 使用

#### 查看安装的所有Node.js版本

```bash
sudo n
```

⬆️⬇️ 选中版本

`回车` 切换选中的版本

`d` 删除选中的版本

`q` 退出

#### 使用n安装Node.js

```bash
sudo n 16.13.0
```
