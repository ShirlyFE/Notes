Safe CSS hacks
==============

原文链接 http://mathiasbynens.be/notes/safe-css-hacks

###1.条件注释的方法添加样式表

```html
    <!--[if lte IE 8]><link rel="stylesheet" href="lte-ie-8.css"><![endif]-->
    <!--[if lte IE 7]><link rel="stylesheet" href="lte-ie-7.css"><![endif]-->
    <!--[if lte IE 6]><link rel="stylesheet" href="lte-ie-6.css"><![endif]-->
```
P.S 条件注释可以通过HTML验证
    CSS验证也可以通过

###2.条件注释类名

一般写在`<html>`或是`<body>`标签上
```html
    <!--[if lt IE 7]><html class="ie6"><![endif]-->
    <!--[if IE 7]>   <html class="ie7"><![endif]-->
    <!--[if IE 8]>   <html class="ie8"><![endif]-->
    <!--[if gt IE 8]><!--><html><!--<![endif]-->
```
```css
    .foo { color: black; }
    .ie8 .foo { color: green; } /* IE8 */
    .ie7 .foo { color: blue; } /* IE7 */
    .ie6 .foo { color: red; } /* IE6 and IE5 (but who cares, right?) */
```


