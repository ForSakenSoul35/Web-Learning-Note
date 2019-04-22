# CSS盒模型
## 盒子概念
1. 行内元素与块级元素
- 常见的行内元素以及块级元素
  * 行内元素  a,img,input,label
  * 块级元素  div form ul dl h1 **p**
- 特性：
  * 行内元素  元素在一行内水平排列 高度由元素的内容决定 height属性不起作用 可以通过设置line-height来设置
  * 块级元素 ，每个元素默认占一行，总在新行上开始 元素垂直排列 高度，行高，以及内外边距都可以控制 宽度默认是它的容器的百分百
- 区别
 * 块级元素可以设置margin，padding，行内元素水平方向的margin padding可以生效。但是竖直方向的margin padding不能生效。
**注意**
div，span，a等标签都是盒子，但是图片，表单元素一律看成文本

## 盒子属性
- width
- height

- padding 内边距 元素的内容到其边界之间的距离
- border
- margin 外边距  元素的外边距 

## 盒子模型
1. 分类
- IE盒子模型
- 标准盒子模型
2. 区别
  - 最重要的区别 是对于宽度和高度的界定
    在IE盒子中，宽度等于 内容的宽度+水平方向上的padding+border 高度等于 内容的宽度+垂直方向上的padding+border
    在标准盒子中  宽度就是内容的宽度  高度就是内容的高度
  - 目前主流浏览器中 使用标准盒子较多
3. 转化
  通过box-sizing设置
  默认属性值：
  - content-box  标准盒子模型
  - border-box IE盒子模型
4. 注意
盒子模型的差异 主要应用在 为了不改变盒子最终宽高 通过设置IE盒子模型 
宽度增加 padding就要减少 padding增加 宽度就要减少

<!-- 
参考文献：
https://www.jeffjade.com/2015/06/24/2015-06-24-css-block-inline/

 -->