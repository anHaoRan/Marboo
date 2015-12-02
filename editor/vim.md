# Mac Vim on Terminal

> 记录配置记录，不想每次都反复查阅文档修改了

### 傻瓜教程

[https://github.com/ma6174/vim](https://github.com/ma6174/vim)

教程中以ubuntu为例，mac上安装使用[brew](http://brew.sh/)安装即可，下面重新列举下安装步骤

* $ brew install ctags
* $ cd ~/ && git clone git://github.com/ma6174/vim.git
* $ rm -rf .vim "如果本地存在.vim文件夹，先删除
* $ mv ~/vim ~/.vim
* $ mv ~/.vim/.vimrc ~/
* $ git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
* 打开vim, 运行:BundleInstall
* 重新打开vim即可

### 设置tab

教程中tab设置长度为4，可以进入`~/.vimrc`中修改为2

### 设置新的主题颜色

设置新的meterial主题[hybrid_material](https://github.com/kristijanhusak/vim-hybrid-material)

使用方法

* 拷贝配色主题文件进入vim配色文件夹

```shell
$ cd ~/ && git clone https://github.com/kristijanhusak/vim-hybrid-material.git
$ cd ~/vim-hybrid-material/colors/
$ cp hybrid*.vim ~/.vim/colors
```

* 设置主题

进入`~/.vimrc`，插入以下代码

```viml
"生效加粗
"let g:enable_bold_font = 1
"设置主题
colorscheme hybrid_material
```

### 给VIM配置powerline状态栏

具体使用方法见[powerline.md](../iterm2/powerline.md)


