# mac下安装powerline

教程来源：[http://cenalulu.github.io/linux/mac-powerline/](http://cenalulu.github.io/linux/mac-powerline/)

> powerline是一个stateless status line，即一个全局状态/提示栏

### 开始Mac上安装powerline

```shell
$ python -v "查看python版本，我的是2.7
$ sudo easy_install pip "安装新的python包安装工具，但是这个pip工具我安装powerline老是报错
$ easy_install powerline-status " 改用安装powerline
$ pip show powerline-status "查看powerline所处的具体路径
```

### 配置字体

```shell
$ git clone https://github.com/powerline/fonts.git
$ cd fonts
$ ./install.sh
```

打开iterm2, 选择菜单：Preferences > Profiles > text

**Regular Font** 和 **Non-ASCII Font** 均选为原来字体 For powerline的字体

### 配置VIM

进入~/.vimrc 插入一行代码

```viml
set rtp+=/Library/Python/2.7/site-packages/powerline/bindings/vim
```

重启vim即可看到效果
