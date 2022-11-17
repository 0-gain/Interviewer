# HTML
## 认识HTML
### HTML是什么？
- 超文本标记语言(HyperText Markup Language,简称HTML)是一种用于创建网页的标准标记语言
- HTML元素是构建网站的基石

### 什么是标记语言(markup language)?
- 由无数个标记(标签、tag)组成
- 是对某些内容进行特殊的标记，以供其他解释器识别处理
- 由标签和内容组成的称为元素

### 什么是超文本(Hyper Text)呢？
- 表示不仅仅可以插入普通的文本，还可以插入图片、音频、视频等内容
- 还可以表示超链接(HyperLink),从一个网页跳转到另外一个网页

## HTML文件的特点
### 扩展名
- HTML文件扩展名：``.htm\.html``
- ``.htm``是历史遗留问题，现在都是``.html``为后缀

## 元素
### 什么是元素？
- HTML本质上是由一系列的元素(Element)构成的；
- 元素是网页的一部分
- 一个元素可以包含一个数据项、一块文本、一张照片，或者什么也不包含
- https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element

### 元素的组成
- 由开始标签 + 属性 + 内容 + 结束标签
  - ``<p class="paragraph">这是一个段落 </p>``
  
### 元素的属性
- 公共的属性，每一个元素都可以设置
  - 比如class、id、title属性
- 特有的属性
  - 比如meta元素的charset属性、img元素的alt属性

### 元素的嵌套关系

- 元素除了是文本之外，还可以是其他元素，这样就形成了元素的嵌套

- ![image-20221117221542246](C:\Users\again\AppData\Roaming\Typora\typora-user-images\image-20221117221542246.png)





## HTML结构分析

- 一个完整的HTML结构包括：文档声明、html元素

- ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    
  </body>
  </html>
  ```

### 文档声明

- ``<!DOCTYPE html>``
- HTML文档声明，告诉游览器当前页面是HTML5页面
- 让游览器用HTML5的标准去解析识别内容
- 必须放在HTML文档的最前面，不能省略，省略了会出现兼容性问题

### html元素

- ``<html>``元素 表示一个HTML文档的根(顶级元素),所以它也成为根元素
  - 其他所有元素必须是此元素的后代
- ``lang属性``
  - 帮助语音合成工具确定要使用的发音
  - 帮助翻译工具确定要使用的翻译规则

### head元素

- 规定文档相关的配置信息(也称为元数据),包括文档标题、引用的文档样式和脚本等
  - 元数据：描述数据的数据
  - 对整个页面的配置
- 网页编码：<span style="color:red">meta元素</span>
  - 可以设置网页的**字符编码**，让游览器更精确地显示每一个文字，<span style="color:red">不设置或者设置错误会导致乱码</span>
  - 一般都使用utf-8编码，涵盖了世界上几乎所有的文字

### body元素

- body元素里面的内容将会在游览器窗口中渲染出来，也就是网页的具体内容和结构

### a元素

- 作用：定义超链接，用于打开新的URL
- 属性
  - href：指定要打开的URL地址，可以是一个本地地址
  - target：指定在何处显示链接的资源
    - _self：默认值，在当前窗口中打开URL
    - _blank：在新的标签页打开URL
    - _parent：配合iframe使用，在父窗口中打开URL
    - _top：配合iframe使用，在最顶层的窗口中打开URL

## 字符实体

- 我们编写的HTML代码会被游览器解析
  - ``<span><heheh</span>``
  - 使用小于号``<``，游览器会将其后的文本解析为一个tag
  - 可以使用字符实体``&lt;``
- HTML实体是一段以字号(&)开头，以分号(;)结尾的文本
  - 实体经常用于显示保留字符(会被解析为HTML代码)和不可见的字符(如“不换行空格”)
  - 可以用实体来代替其他难以用标准键盘键入的字符

## 元素语义化
- 用正确的元素做正确的事情
- 好处
  - 有利于SEO
  - 方便代码维护
  - 减少让开发者之间的沟通成本
  - 能让语音合成工具正确识别网页元素的用途，以便作出正确的反应

