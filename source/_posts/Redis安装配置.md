---
title: Redis安装配置
date: 2022-04-24 03:21:44
tags:  
  - Redis
  - HomeBrew
categories: Redis
---

## 安装 Redis

官网地址：https://redis.io/

### Homebrew 安装 Redis

```bash
brew install redis
```

### 前台启动 Redis

```bash
redis-server
```

![image-20220424033611211](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204243611S7aBLF.png)

要停止 Redis，请输入`Ctrl-C`

### 使用 launchd 启动 Redis

```bash
brew services start redis
```

![image-20220424033701590](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204243701bbqT0O.png)

### 使用 launchd 查看托管 Redis 状态

```bash
brew services info redis
```

![image-20220424033730168](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022042437306tFkG3.png)

### 使用 launchd 重启 Redis

```bash
brew services restart redis
```

![image-20220424100354345](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204240354HrCHS4.png)

### 使用 launchd 停止 Redis

```bash
brew services stop redis
```

![image-20220424033745836](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022042437458TbA6P.png)

---

## 配置Redis

我的配置文件路径是 `·/opt/homebrew/etc/redis.conf`(`command+shift+.`显示隐藏文件)

找不到的可以连接上命令行连接redis后，输入命令查看当前使用的配置文件

```bash
info server
```

![image-20220502221919317](../../../Library/Application%20Support/typora-user-images/image-20220502221919317.png)

![image-20220502224214677](../../../Library/Application%20Support/typora-user-images/image-20220502224214677.png)

### 我这边做的配置：

**logfile**：redis 日志文件，默认没有设置

```tex
logfile /opt/homebrew/var/log/redis/log-redis.log
```

**dir**：redis 数据库文件路径

```tex
dir /opt/homebrew/var/db/redis/
```

**requirepass**：redis密码，默认没有做设置，需要的可以自己加上

```tex
requirepass 123456
```

### 其他的配置（未作修改，需要的可以根据自己情况来更改）

```tex
daemonize        是否为守护模式（是否为后台启动）
pidfile          进程锁文件
port             端口
timeout          客户端超时时间
loglevel         日志级别
databases        数据库数量 
rdbcompression   存储到本地数据库时是否对数据进行压缩（lcf压缩）性能/容量（抉择）
dbfilename       数据库文件名称
```

#### redis日志分为4个级别

Redis4默认的设置为notice，开发测试阶段可以用debug（日志内容较多一般不建议使用），生产模式一般选用notice

1. debug：会打印出很多信息，适用于开发和测试阶段

2. verbose（冗长的）：包含很多不太有用的信息，但比debug要清爽一些

3. notice：适用于生产模式

4. warning : 警告信息

**更新完配置文件之后，重启 redis 使配置生效**

```bash
brew services restart redis
```

## 遇到的问题

![image-20220503225530253](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220503225530x6qK7G.png)

可以看到我这边重启显示成功，但是 redis 实际上并没有跑起来

查看日志`/opt/homebrew/var/log/redis.log`(HomeBrew 创建的)

![image-20220503225446514](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220503225446jwZwbg.png)

![image-20220503225346558](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220503225346dhr9DN.png)

查看日志了解到上面配置的 redis 日志文件的目录没有

![image-20220503225606643](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220503225606BtVA3Q.png)

因为设置的路径不在用户目录里，所以可能没有权限创建文件夹

这里手动创建就好了 (或者修改配置文件，将日志放到用户目录下`/Users/zhoufan/xxxx/log-redis.log`)

![image-20220503225718404](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220503225718JGXivI.png)

![image-20220503225825592](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220503225825LakrQh.png)
