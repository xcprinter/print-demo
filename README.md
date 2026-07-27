##  如何实现



# 曦辰打印机演示页

基于 [index.html](index.html)加上[style.css](style.css)的简单品牌展示页面，用于演示曦辰打印机的核心价值和打印组件调用方式。


### 代码示例

在 data-controller 标签内，可以定义打印内容及其样式。

```html
<div data-controller="print-pos"></div>
```

###
* 打印标题  data-print="text_big"
* 打印内容  data-print="text"
* 打印二维码 data-print="qrcode"


[index.html](index.html) 是一个真实的案例，可以前往[在线预览](https://app-demo.xcprinter.com)
