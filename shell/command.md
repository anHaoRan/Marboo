# 一些有用的命令

### brew

### tldr & cheat

用来查看linux命令使用方法，比如

```shell
$ tldr tar
$ cheat tar
```

安装方法

```shell
$ brew install cheat
$ npm install -g tldr
```

### bugfreejs

自动在JS头部加上神注释，默认支持utf8和GBK编码的js文件。

见地址[https://github.com/ottomao/bugfreejs](https://github.com/ottomao/bugfreejs)

### 开始Chrome非安全模式

```shell
# Chrome < 48
open /Applications/Google\ Chrome.app --args -disable-web-security

# Chrom > 48
open -a Google\ Chrome --args --disable-web-security --user-data-dir
```

### homeshick

[教程](https://mine260309.me/archives/1220)

```shell
git clone git://github.com/andsens/homeshick.git $HOME/.homesick/repos/homeshick
printf '\nsource "$HOME/.homesick/repos/homeshick/homeshick.sh"' >> $HOME/.bashrc
. ~/.bashrc
```