# CSS 选择器
 

## 基本选择器
- 通配选择器
- 标签选择器
- id
- class

多元素的组合选择器
- 并集 多元素选择器 E,F  用逗号隔开
- 交集选择器  #div.id  选择器之间没有任何的连接符号，可以是标签名也可以id和class名
- 后代 E F 用空格隔开 
- 子代 E>F 用大于号隔开 匹配E元素的所有F子元素
- 毗邻元素  E+F 匹配所有紧随E元素之后的所有F元素
- 兄弟元素 E~F 匹配任何在E元素之后的同级F元素（CSS3）

**对比：毗邻元素 和兄弟元素对比**


## 属性选择器：
CSS2.1
- E[att] 匹配所有具有att属性的E元素 不考虑具体的属性值
- E[att = "val" ] 匹配所有属性值等于val 的E元素  E[ foo ="warning" ]
- E[att ~="val" ]  匹配所有att属性具有多个空格分隔的值 其中一个值等于"val"的E元素
- E[att |= "val"] 匹配所有att属性具有多个连字符分隔（类似 这样hello-world-xhb）的值 其中一个值以"val"的E元素  主要用于lang属性 比如 "en" "en-us"等

CSS3 
- E[att ^="val"] 属性att的值以"val"开头的元素
- E[att $="val"] 属性att的值以"val"结尾的元素
- E[att *="val"] 属性att的值包含"val"的元素
 

##伪类选择器
CSS2.1
- E:first-child 匹配父元素的第一个子元素

- E:link  匹配所有未被点击的链接
- E:visited 匹配所有已被点击的链接
- E:active 匹配鼠标已经将其按下 但是还未离开的E元素
- E:hover 匹配鼠标悬停（鼠标经过）的E元素

**补充 这四个选择器写的顺序**

- E:fpcus 匹配获取当前焦点的E元素
- E:lang(c) 匹配lang属性等于c的E元素



CSS3 
表单伪类
- E:enabled 匹配表单中激活的元素
- E:disabled 匹配表单中禁用的元素
- E:checked 匹配表单中被选中的radio或者checkbox元素

**表单伪类 需要再理解**
结构性伪类
- E:last-child  匹配父元素的最后一个元素
- E:only-child 匹配父元素下仅有的一个子元素


- E:nth-child(n)  匹配其父元素的第n个子元素，第一个编号为1
- E:nth-last-child(n) 匹配其父元素的倒数第n个子元素，第一个编号为1

- E:nth-of-type(n) 与:nth-child()作用类似，但是仅匹配使用同种标签的元素
- E:nth-last-of-type(n) 与:nth-last-child() 作用类似，但是仅匹配使用同种标签的元素
<!-- 匹配同种标签  -->


- E:first-of-type 匹配父元素下使用同种标签的第一个元素
- E:last-of-type  匹配父元素下使用同种标签的最后一个元素
- E:only-of-type 匹配父元素下使用同种标签的唯一一个子元素

- E:root 匹配文档的根元素，对于HTML文档，就是HTML元素
- E:empty  匹配一个不包含任何子元素的元素  文本节点也被看做子元素
**结构伪类 需要再理解**
反选伪类
- E:not(s) 匹配不符合当前选择器的任何元素  :not(p){..}

## 伪元素
一个选择器只能使用一个伪元素 伪元素必须紧跟在语句中的简单选择器/基础选择器后面
必须使用双引号  但是由于旧版本的W3C规范未对此进行区分 因此目前绝大多数的浏览器 都同时支持这两种写法表示伪元素
- E::before  在E元素之前插入生成的内容
- E::after 在E元素之后插入生成的内容

- E::first-line 匹配E元素的第一行
- E::first-letter 匹配E元素的第一个字母
- E::selection  匹配用户被选中的元素



