## 表单系列元素

* HTML5 input appearance

> [http://exisweb.net/css-input-number-firefox](http://exisweb.net/css-input-number-firefox)

```css
/*  解决在微信浏览器上出现的number输入样式的问题  */
::-webkit-inner-spin-button { -webkit-appearance: none;}
::-webkit-outer-spin-button { -webkit-appearance: none;}

input[type="number"] {
  -moz-appearance: textfiled;
  -webkit-appearance: none;
}
```