# sublime text 编辑器

## install Package Control

> Menu: View(视图) > Show Console(显示控制台)

```shell
# Sublime Text 2 代码
import urllib2,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')

# Sublime Text 3 代码
import urllib.request,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

## some popular plugin

> Ctrl(Command) + Shift + P

* Emmet
* HTML-CSS-JS Prettify
* Sublime​Code​Intel 代码自动提示补全
* AutoFileName
* jQuery
* DocBlockr 代码快速注释
* BracketHighlighter 匹配标签高亮
* IMESupport 解决中文输入框不跟随

## Mac 上命令行启动编辑器

```shell
$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin 

$ sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

此时就可以通过`subl .`在sublime中打开当前文件夹


## 自定义快捷键

> Ctrl + ~ / Show Console
> 
> `sublime.log_commands(True)`


##  我的用户配置文件
```json
{
  "bold_folder_labels": true,
  "caret_style": "smooth",
  "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
  "default_line_ending": "unix",
  "disable_tab_abbreviations": true,
  "draw_minimap_border": true,
  "draw_white_space": "all",
  "file_exclude_patterns":
  [
    ".DS_Store",
    "Desktop.ini",
    "*.pyc",
    "._*",
    "Thumbs.db",
    ".Spotlight-V100",
    ".Trashes"
  ],
  "folder_exclude_patterns": [
    ".*",
    "node_modules"
  ],
  "font_face": "Input Mono",
  "font_options":
  [
    "gray_antialias"
  ],
  "font_size": 18,
  "highlight_line": true,
  "ignored_packages":
  [
    "Markdown",
    "Vintage"
  ],
  "indent_guide_options":
  [
    "draw_normal",
    "draw_active"
  ],
  "line_padding_bottom": 5,
  "line_padding_top": 5,
  "margin": 2,
  "tab_size": 2,
  "theme": "Material-Theme.sublime-theme",
  "translate_tabs_to_spaces": true
}
```

