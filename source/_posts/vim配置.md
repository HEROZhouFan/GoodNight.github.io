---
title: vim配置
date: 2022-05-01 16:33:27
tags:
  - Vim
categories: Vim
---

## 配置

```bash
vim ~/.vimrc
```

我自己做的配置

```tex
set number "显示行号"
syntax on "代码高亮"
set mouse=a "启用鼠标"
set t_Co=256 "启用256色"
filetype indent on "开启文件类型检查，并且载入与该类型对应的缩进规则"
set cursorline "光标所在的当前行高亮"
set incsearch "输入搜索模式时，每输入一个字符，就自动跳到第一个匹配的结果"
set ignorecase "搜索时忽略大小写"
```

**注意后面注释是`双引号`，配置成`#`会有问题**

更多其他配置参考

https://www.ruanyifeng.com/blog/2018/09/vimrc.html
