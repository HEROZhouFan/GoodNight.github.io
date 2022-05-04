---
title: HomeBrew命令
date: 2022-04-24 03:00:58
tags: HomeBrew
categories: HomeBrew
---

### 查看brew版本

```bash
brew -v
```

![image-20220424031326759](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204241326A84VRW.png)

### 安装软件

```bash
brew install wget
```

### 卸载软件

```bash
brew uninstall wget
```

### 搜索软件

```bash
brew search wget
```

![image-20220424031411228](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204241411uaOgK5.png)

### 查看brew安装的软件

```bash
brew list
```

![image-20220424031431314](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022042414312LDkqW.png)

### 查看软件安装路径

```bash
brew list wget
```

![image-20220424031508656](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204241508SM6Ub8.png)

### 更新brew

```bash
brew update
```

### 查看哪些安装包需要更新

```bash
brew outdated
```

### 更新所有包

```bash
brew upgrade 
```

### 更新指定的包

```bash
brew upgrade wget
```

### 查看可清理的旧版本包，不执行实际操作

```bash
brew cleanup -n
```

### 清理所有包的旧版本

```bash
brew cleanup
```

![image-20220424031647830](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/2022042416471HemOf.png)

### 清理指定包的旧版本

```bash
brew cleanup $FORMULA
```

### 查看已安装的包的依赖，树形显示

```bash
brew deps --installed --tree
```

![image-20220424031746627](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204241746svWULe.png)

### 删除某个包

```bash
brew rm $FORMULA
```

### 删除所有版本

```bash
brew uninstall --force $FORMULA
```

### 锁定某个包

```bash
brew pin $FORMULA
```

### 取消锁定

```bash
brew unpin $FORMULA
```

### 浏览器打开Homebrew官网

```bash
brew home
```

### 查看安装了包数量，文件数量，和总占用空间

```bash
brew info
```

![image-20220424031820044](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204241820SjnSjZ.png)

### 显示某个包的信息

```bash
brew info $FORMULA
```

![image-20220424031845306](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202204241845XgX9sX.png)

