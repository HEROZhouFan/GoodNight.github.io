---
title: iTerm2 + Oh My Zsh安装配置
date: 2022-05-01 16:17:35
tags:
  - 环境搭建
  - 软件安装
  - iTerm2
  - Oh My Zsh
  - HomeBrew
  - Shell
  - Dracula
categories: iTerm2
---

## HomeBrew cask 安装 iTerm2

**高版本和低版本 HomeBrew cask 命令稍有不同**

高版本

```bash
brew install --cask iterm2
```

低版本

```bash
brew cask install sourcetree
```

## iTerm2 设置

### 将 iTerm2 设置为默认 iTerm

![image-20220502205627857](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220502205635AEAt6X.png)

### 关闭 ITerm2 的确认关闭弹窗提醒

![image-20220502205921543](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220502205927rMryIp.png)

---

## zsh

### 查看 zsh 版本 (Mac 自带)

```bash
zsh --version
```

## 如果没有安装 zsh，使用 HomeBrew 安装

```bash
brew install zsh
```

### 如果有安装，可以更新至最新版本

```bash
brew upgrade zsh
```

### 安装完成以后，将zsh设置为默认的Shell

```bash
chsh -s /bin/zsh
```

---

## Oh My Zsh

**提前备份好`~/.zshrc`文件，不然会被覆盖掉**

### 首先安装 wget

```bash
brew install wget
```

### wget 安装 Oh My Zsh

```bash
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh\n
```

---

## 修改默认 Shell为 zsh

### 查看所有的 shell

```bash
cat /etc/shells
```

![image-20220501223249296](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501223249oOuGM9.png)

### 查看当前窗口使用的 shell

```
exho $0
```

![image-20220501223346779](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501223346lGUofr.png)

### 修改系统默认 shell为 zsh

```bash
chsh -s /bin/zsh
```

---

## Oh My Zsh 插件

### zsh-syntax-highlighting

作用：代码高亮，平常用的`ls`、`cd` 等命令输入正确会绿色高亮显示，输入错误会显示其他的颜色

安装

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

下载完成后，需在配置文件中配置生效（配置方法在下方⬇️）

### zsh-autosuggestions

作用：代码补全   按 ⬆️或➡️即可补全

安装

```bash
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

下载完成后，需在配置文件中配置生效（配置方法在在下方⬇️）

![image-20220501225133880](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501225133rpLU1f.png)

### z

作用：切换目录

安装  自带，需在配置文件中配置生效（配置方法在在下方⬇️）

![image-20220501230303640](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501230303uSnSwB.png)

### d 

作用：目录切换

安装 自带，默认已开启

![image-20220501225924807](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501225924sQAxyT.png)

### sublime

作用：在命令行使用 `Sublime Text` 打开文件、项目

| 命令        | 作用                          |
| ----------- | ----------------------------- |
| st          | 打开 sublime                  |
| st + 文件夹 | 打开该文件夹                  |
| st + 文件   | 打开该文件                    |
| stt         | 打开当前的文件夹，相当于 st . |
| sst         | 管理员权限 相当于 sudo st     |

安装 自带，需在配置文件中配置生效（配置方法在在下方⬇️）

---

## Oh My Zsh 配置

### 配置插件生效

`vim` 编辑配置文件`~/.zshr`

```bash
vim ~/.zshrc
```

找到`plugins`标签，添加自己需要的插件

```tex
plugins=(
    git
    z
    sublime
    zsh-autosuggestions
    zsh-syntax-highlighting
  )
```

重新加载配置文件

```bash
source ~/.zshrc
```

---

## Oh My Zsh 快捷键

- 鼠标选中即复制;
- command + d 垂直分屏
- command + shift + d 水平分屏
- command + shift + h 打开剪切板(复制历史)
- command + ; 命令自动完成
- command + shift + ; 查看历史命令
- command + option + b 按键回放(输入命令回放, 通过时间线)

---

## 更换 zsh 主题为 Dracula

1. 下载主题文件

   ```bash
   git clone https://github.com/dracula/zsh.git
   ```

2. 将下载的`dracula.zsh-theme`文件 (找不到全局搜索下) 放到`/Users/zhoufan/.oh-my-zsh/themes`目录下

   （`command + shift + .` 显示隐藏文件）

   ![image-20220501233743796](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501233743O8A3qT.png)

3. 将`async.zsh` 文件放到`/Users/zhoufan/.oh-my-zsh/lib`目录下

   ![image-20220501234732269](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220501234732bNQlIC.png)

4. 修改zsh主题。编辑~(用户名)下.zshrc文件，修改ZSH_THEME为"dracula"

```bash
vim ~/.zshrc
```

修改ZSH_THEME为"dra

```tex
ZSH_THEME="dracula"
```

加载配置文件

```bash
source ~/.zshrc
```

---

## 更换 iTerm2 主题为 Dracula

下载

```bash
git clone https://github.com/dracula/iterm.git
```

打开 iTerm2 偏好设置

![image-20220502001758622](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220502001758v2xPaK.png)

最下方 import，将`Dracula.itermcolors`文件导入进来

![image-20220502002247276](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220502002247rVjLhX.png)

选择应用，完成

##  iTerm2一键ssh连接远程服务器配置

1. 编写一个文件，内容如下，把对应的中文改成你的服务器相关内容就行，这里我将其编写为txt文本文件，放到用户目录下的.zsh文件夹下(~/.zsh/aliyun.txt)(command+shift+.显示隐藏文件夹)

   ```tex
   #!/usr/bin/expect -f
     set user 用户名
     set host ip地址
     set password 密码
     set timeout -1
   
     spawn ssh $user@$host
     expect "*assword:*"
     send "$password\r"
     interact
     expect eof
   ```

2. 打开iTerm2，打开设置(Preferences)，点击Profiles，点左下角+

   ![zsh_ssh](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/20220502002505Bcf7OA.png)

3. 以后在终端界面直接点击即可连接到服务器

   ![img](https://raw.githubusercontent.com/HeroZhouFan/uPic/master/uPic/202205020026015NJZAg.jpeg)

---

## 关闭 Oh My Zsh 自动更新

每天第一次打开Terminal的时候都会卡顿一下，原因是因为ZSH每天会在第一次打开时进行自动更新检测

```bash
vim ~/.zshrc
```

查找`DISABLE_AUTO_UPDATE`，将其注释打开，使其生效

```bash
DISABLE_AUTO_UPDATE="true"
```

重新加载配置文件

```bash
source ~/.zshrc
```

此时，再次打开Terminal的时候就不会出发自动更新检查。
那么如何手动更新呢？请执行下面的命令即可：

```bash
upgrade_oh_my_zsh
```

当然也可以通过下面的方式来进行检查更新：

```bash
zsh ~/.oh-my-zsh/tools/check_for_upgrade.sh
```
