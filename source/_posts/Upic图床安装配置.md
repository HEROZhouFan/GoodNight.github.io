---
title: Upic图床安装配置
date: 2022-05-01 16:16:38
tags:
  - 软件安装
  - Upic
  - GitHub
  - Typort
categories: Upic
---

## GitHub创建仓库

![image-20220501170723268](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205010723Q3oBC4.png)

![image-20220501171027455](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205011027u4cBiC.png)

仓库创建完成，进入`Settings`

![image-20220501171253805](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205011326Zyk2lO.png)

拉到最下方

![image-20220501171334062](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205011334nC7UF1.png)

创建一个密钥

![image-20220501171457123](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205011457jAGvbo.png)

![image-20220501173413296](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205013413dJj97b.png)

![image-20220501172219357](../../../../Downloads/202205012219IkpHYS.png)

**创建密钥成功，记得复制保存**

![image-20220501173512517](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205013512kHktj4.png)

---

## Upic配置GitHub仓库

打开Upic`偏好设置`

配置用户名，仓库名，分支，Token（刚才配置生成的字符串），存储路径

为防止图片重名，这边设置时间+随机数.后缀的格式

```tex
 uPic/{year}{month}{day}{hour}{minute}{second}{random}{.suffix}
```

![image-20220501173721867](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205013721idBZvR.png)

上面的图配置的是 jsDelivr CDN 加速，当 jsDelivr CDN 挂了图片会加载不出来，所以我后来取消了 jsDelivr CDN加速，并将域名改成了

```tex
https://raw.githubusercontent.com/HeroZhouFan/uPic/master
```

![image-20220502210504440](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220502210514gdAg6Q.png)

---

## Typort配置图床

打开Typort`偏好设置`

![image-20220501174234274](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501174234mJYZqQ.png)
