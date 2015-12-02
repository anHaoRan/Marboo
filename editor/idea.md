# jetbrains 系列主题配色

> 配置为material-theme

[https://github.com/ChrisRM/material-theme-jetbrains](https://github.com/ChrisRM/material-theme-jetbrains)

## 直接拷贝教程中的说明文档

安装 

* Open the **Settings/Preferences** dialog (OSX/Unix: ⌘,, Windows: Ctrl+Alt+S)
* In the left-hand pane, select **Plugins**.
* Click **Browse repositories...** and search for `Material Theme UI`
* Click **Install plugin** and confirm your intention to download and install the plugin.
* Click OK in the Settings dialog and restart for the changes to take effect.

设置主题颜色

  This plugin will not set the new color scheme for you, as that would cause a couple problems. You need to set the new color scheme manually:

* Open the **Settings/Preferences** dialog again.
* In the left-hand pane, select **Editor** -> **Colors & Fonts**.
* In the **Scheme** dropdown, you'll find 3 new schemes: `Material Theme - Default`, `Material Theme - Darker` and `Material Theme - Lighter`.
* Choose the scheme you like and hit **Apply** and **OK**.
* Shortcut: Ctrl+' (that's a backtick) then hit 1. Color scheme and select your desired color scheme.'

# Mac WebStorm 11 打不开

> 之前WebStorm9购买的license一年到了，今天重新续费，晚上回来下了WebStorm11，安装后一直报错，说打不开

解决方案：

进入应用程序文件夹，找到WebStorm，右击显示包内容，Contents > MacOS > webstorm 运行

此时输入license也和以前不一样了，需要输入新的license，之前9的license不再可用。

进入license，点击Assign，输入email，firstName，lastName，会生成一个txt，把txt里面的内容复制到license里即可
