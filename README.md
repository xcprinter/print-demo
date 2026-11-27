# 蓝牙打印能力集成
1 分钟在你的 Web 页面接入蓝牙打印能力！

* 你不需要写任何 js 代码
* 用户也无需安装驱动或额外软件，由我司提供的原生框架采用 js 注入的方式引入了必要的依赖
* 点击按钮即可打印，你在页面中指定的按钮我们会根据情况变动按钮文字引导用户配置打印机

## 工作流程
用户在网页上配置打印内容
配置打印按钮 
浏览器通过 `print-pos` 组件识别并连接原生能力
点击按钮直接调用打印机完成小票（标签）打印

## 如何实现
在 `data-controller` 标签内，通过 `data-print` 和 `data-action` 属性定义打印内容和触发行为。

### 打印属性
* `data-controller="print-pos"` 声明打印组件容器
* `data-print="text_big"` 打印标题
* `data-print="text"` 打印文本内容
* `data-print="qrcode"` 打印二维码
* `data-button-id="print"` 指定 id 为 `print` 的元素触发打印操作

## 打印具体数据
```html
<button
  data-action="click->print-pos#printData"
  data-content="1f,2d,35,04,00,05,c8,00"
>设置步进</button>
```

## 打印
```html
<button data-action="click->print-pos#printInner">
  <div data-print="barcode" class="display-none">012345789</div>
  <span>打印条形码</span>
</button>
```

### 综合示例
```html
<section data-controller="print-pos" data-button-id="print">
  <div class="text-centered">
    <h1 data-print="text_big">打印标题</h1>
    <h2 data-print="text">打印普通文本</h2>
    <h2 data-print="qrcode">打印为二维码</h2>
  </div>
  <button id="print">打印</button>
</section>
```

[index.html](index.html) 是一个完整的真实案例，可前往 [在线预览](https://app-demo.xcprinter.com) 查看效果。
