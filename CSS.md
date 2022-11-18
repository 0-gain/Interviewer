# CSS
## 认识CSS
- CSS标识层叠样式表，是为网页添加样式的代码
- CSS是一种语言吗？
  - MDN解释：CSS也不是真正的编程语言，甚至不是标记语言，它是一门样式表语言
  - 维基百科解释：是一种计算机语言，但是不算是一种编程语言
- CSS的出现是为了美化HTML的，并且让结构(HTML)与样式(CSS)分离

## 使用CSS
- 语法：
  - 属性名:属性值
  - ``color:red;``
- 应用形式
  - 内联(inline style)---行内样式
    - ``<p style="color:red">我是p元素</p>``
  - 内部样式表、文档样式表、内嵌样式表
    - 将CSS放在HTML文件``<head>``元素里的``<style>``元素中
  - 外部样式表
    - 将CSS编写一个独立的文件中，并且通过``<link>``元素引入进来
    - 使用``@import url(路径)``导入CSS文件

## 选择器
- 属性选择器
  - 拥有某一个属性``[title]``
  - 属性等于某个值``[title = val]``
- 后代选择器
  - 所有的后代(直接/间接后代)
  
  - 选择器之间以**空格**分隔
  
  - ```html
      <head>
        <style>
          div span {
            color: red;
          }
        </style>
      </head>
      <body>
        <div>
          <span>div下面的span</span>
          <ul>
            <li class="first"><span>1</span></li>
            <li><span>2</span></li>
            <li><span>3</span></li>
            <li><span>4</span></li>
            <li><span>5</span></li>
          </ul>
          <p>我是p元素</p>
        </div>
    </body>
      
    ```
  
- 后代选择器(直接子代选择器)
  - 选择器之间以``>``分割
    - ``div > span``
- 兄弟选择器(相邻兄弟选择器)
  - 使用符号``+``连接
    - ``.first + li``
- 普通兄弟选择器
  - 使用符号``~``连接
    - ``.first ~ li``
- 交集选择器(两个选择器精密连接)
  - 需要同时符合两个选择器条件
  - 通常为了精准的选择某一个元素
  - ``li.first``
- 并集选择器
  - 符合一个选择器条件就可以了(两个选择器以,号分割)
  - ``span,ul,p``
  

## 伪类
- 伪类是选择器的一种,它用于选择处于特定状态的元素
- 通常是以``单冒号``的形式

### 动态伪类
- ``:link、:visited、:focus、:hover、:active``
- ``a:link``未访问的链接
- ``a:visited`` 已访问的链接
- ``a:focus`` 被聚焦的状态
- ``a:hover``  鼠标悬浮到链接
- ``a:active`` 激活的链接(鼠标在链接上长按住未松开)
- **``:hover``必须放在``:link``和``:visited``后面才能完全生效**
- **``:active``必须放在``:hover``后面才能完全生效**
- 顺序link,visited,focus,hover,active
- 直接给a元素设置样式,相当于给a元素的所有动态伪类都设置了



## 伪元素
- 可以使用双冒号,和单冒号的形式,但是一般为了区分伪元素,一般使用双冒号
- ``::before、::after、::first-line、::first-letter``
- ``::before、::after``用来在一个元素的内容之前或之后插入其他内容(content)必须要存在,默认是块级元素