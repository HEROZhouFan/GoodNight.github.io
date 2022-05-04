---
title: Docker安装配置
date: 2022-05-04 20:26:03
tags:
  - 环境搭建
  - 软件安装
  - Docker
categories: Docker
---

## 安装

官网地址：https://www.docker.com/

![image-20220504210805816](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220504210805mHR4T5.png)

![image-20220504210841580](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220504210841bKpDh1.png)

## 配置

### 配置阿里云镜像源

![image-20220504211821872](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220504211821M78G2H.png)

添加镜像配置

```json
,
  "registry-mirrors": [
    "https://0wg8f6sb.mirror.aliyuncs.com"
  ]
```

完整配置如下（包含docker默认配置）

```json
{
  "builder": {
    "gc": {
      "defaultKeepStorage": "20GB",
      "enabled": true
    }
  },
  "experimental": false,
  "features": {
    "buildkit": true
  },
  "registry-mirrors": [
    "https://0wg8f6sb.mirror.aliyuncs.com"
  ]
}
```

