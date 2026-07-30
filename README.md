# 打印机集成
1 分钟接入打印平台！


## 功能说明
让你的网站直接连接打印机，无需安装驱动或额外软件，点击按钮即可打印。

## 工作流程 

用户在网页上配置打印内容
配置打印按钮 

→ 浏览器通过 `print-pos` 组件
直接调用打印机 → 小票/标签秒出

### 适用场景

* 外卖平台——骑手取餐时一键打印小票
* 便利店/超市——收银台打印价签和购物清单
* 快递驿站——扫码即打快递面单


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
