# JAVASCRIPT

> Javascript看似简单，但是里面有太多有意思和未知的东西需要我去探索，没有完整读过其API，先记录一些我遇到的“生僻”词汇

------------------

### 正则表达式中的`()`、`|`、`$1`的意义和作用

### `>>`、`~~`、`|`等特殊运算的意思

### `location`有哪些属性，分别代表什么，具备哪些特殊效果和事件

### encode 一共有几种方法，分别有什么效果 

### 以下方法的兼容性

* `querySelector` / `querySelectorAll`
* `localStorage`

### `history` 对象下的一些高级用法

### `window`对象下特殊属性的的全部内容

* `onbeforeunload`
* `onunload`

### unicode字符的表示

js中var s = '\u8FC7'表示‘过’

css中content: '\8FC7'表示‘过’

js中如何把一个中文转换成该编码：

```javascript
var chinese = '中文示例';

function toUnicode(str) {
  return str.split('').map(function (c) {
    return '\\u' + c.charCodeAt(0).toString(16).toUpperCase();
  }).join('');
}

toUnicode(chinese); // \u4E2D\u6587\u793A\u4F8B
```

