<h2 align=center>曦辰打印机</h2>
<h4 align=center>
🚀导航：<a href="#快速开始">快速开始</a> • <a href="#曦辰打印机演示页">演示页说明</a> • <a href="#如何实现">如何实现</a>
</h4>


## 🚀快速开始

* **部署源码：**
```
git clone git@github.com:xcprinter/xcprinter.github.io.git
```
* **直接点击 `index.html`[index.html](index.html) 即可在浏览器中预览，或部署到任意静态服务器。**
* 页面适配桌面端和移动端，`@media (max-width: 480px)` 自动切换布局。
* 代码问题请提 [issue](https://github.com/xcprinter/xcprinter.github.io/issues)。


## 曦辰打印机演示页

基于 [index.html](index.html) + [style.css](style.css) 的品牌展示页面，用于演示曦辰打印机的核心价值及打印组件调用方式。

### 文件结构

* `index.html` — 页面结构，包含打印组件标签
* `style.css` — 独立样式，暖色系主题，响应式适配

### 页面设计

* 页面背景 — `linen` 暖色底
* 卡片容器 — `rgb(250, 231, 212)` 米色背景、圆角 8px、左右全铺
* 品牌标题 — `Tomato` 番茄色、字号 35px、字间距 4px
* 副标题 — `maroon` 栗色、字号 20px、行高 1.6
* 打印按钮 — 白字红底、圆角 6px、hover 变深红 `#c1121f`
* 移动端适配 — body 内边距清零、卡片圆角取消、按钮撑满宽度


## 如何实现

在 `data-controller` 标签内，通过 `data-print` 和 `data-action` 属性定义打印内容和触发行为。

### 代码示例

```html
<section class="card" data-controller="print-pos">
  <div class="text-centered">
    <h1 data-print="text">曦辰打印机</h1>
    <h2 data-print="text">绕过巨头抽成和垄断</h2>
    <h2 data-print="text">让小商家和骑手更赚钱</h2>
  </div>
  <button data-action="print-pos#print">打印</button>
</section>
```

### 打印属性

* `data-controller="print-pos"` — 声明打印组件容器
* `data-print="text_big"` — 打印标题
* `data-print="text"` — 打印文本内容
* `data-print="qrcode"` — 打印二维码
* `data-action="print-pos#print"` — 触发打印操作

[index.html](index.html) 是一个完整的真实案例，可前往 [在线预览](https://app-demo.xcprinter.com) 查看效果。
