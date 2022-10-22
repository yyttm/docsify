<p align="center">
    <a href="https://yyttm.github.io/web2/" target="_blank">
        <img src="https://c2.im5i.com/2022/09/07/5JRSG.png" width=""/>
    </a>
</p>

---

# HTMl5

## 基本语法概括

+ HTML标签是由尖括号包围的关键词，例如`<html>`
+ HTML标签通常是成对出现的由“开始标签”和“结束标签”两部分组成，例如`<html>`和`</html>`
+ 有个别标签的是单独出现的，由一个标签组成，例如`<hr />`

## 两类双标签

双标签分为两类，==包含关系（父子关系）==和==并列关系==

**包含关系**

```html
<head>
	<title></title>
</head>
```

**并列关系**

```html
<head></head>
<body></body>
```

## HTML基本构成标签

每个网页都会由一个基本标签（骨架标签）页面内容页是在这些基本标签上书写，html页面也被称为html文档

```html
<html>  # html标签，根标签 
    <head> # 文档的头部，head必须设置的标签是title
        <title></title> # 文档的标题
    </head>
    <body></body> # 文档主题，页面内容都是放在body里
</html>
```

## 骨架标签

```html
<!DOCTYPE html> #文档类型声明，告诉浏览器用哪种html版本来显示网页
# 注意！
# <!DOCTYPE>声明位于文档中最前面的位置，处于<html>标签的之前
# <!DOCTYPE>不是一个HTML标签，它就是文档类型声明标签
<html lang="en"> # 显示语言，用来定义当前文档显示的语言
# 1、en定义语言为英语
# 2、zh-CN定义语言为中文
<head>
    <meta charset="UTF-8"> # 字符集，以便计算机能够识别和储存各种文字
# 在<head>标签中可通过<meta>标签的charset属性规定html应该使用哪种字符编码
#charset常用的值有：GB2312、BIG5、GBk和UTF-8其中UTF-8被成为万国码，基本包括了全世界所有国家需要的字符
#注意：上面语法是必须要写的代码，否则会引起乱码的情况
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title> #标题标签，双标签
</head>
<body>
    
</body>
</html>
```

## 常用标签

**标签语义**

简单理解就是指标签的含义，根据标签的语义，在合适的地方给一个最合理的标签，可以让页面结构更清晰

### 标题标签

为了使网页更有语义化，经常会用到标题标签，HTML提供了6个等级的网页标签及`<h1>`-`<h6>`

```html
<h1>这是一级标题</h1>
<h2>这是二级标题</h2>
<h3>这是三级标题</h3>
<h4>这是四级标题</h4>
<h5>这是五级标题</h5>
<h6>这是六级标题</h6>
```

标签语义：作为标题使用并依据重要性递减

特点：

+ 加了标题的文字会变得加粗字号也会依次变大
+ 一个标题独占一行

### 段落标签

在网页中要把文字有条理的显示出来，就需要将这些文字分段显示。在html标签中`<P>`标签用于定义段落，它可以将整个页面分为若干个段落

```html
<p>这是一个段落标签</p>	
```

标签语义：可以把html文档分割为若干个段落

特点：

+ 文本在一个段落中会根据浏览器窗口大小自动换行
+ 段落之间保有空隙

### 换行标签

在html中，一个段落的文字会从左到右依次排列，直到浏览器口的右端然后才能自动换行如果希望某段文本强制换行显示就需要使用换行标签` <br />`

```html
<br />
```

标签语义：强制换行

特点：

+ 是个单标签
+ 是简单的开始新的一行，段落不一样段落之间会插入一些垂直的间距

### 字体标签

在网页中，有时候需要为文字设置粗体，斜体，或下划线等效果，这时候需要用到html中的文本格式化标签，使文字以特殊的方式显示。

标签语义：突出重要性

```html
<strong>加粗</strong>
<b>加粗</b>
<em>倾斜</em>
<i>倾斜</i>
<del>删除线</del>
<s>删除线</s>
<ins>下划线</ins>
<u>下划线</u>
```

### `<div>`和`<span>`标签

`<div>`和`<span>`是没有语义的，它们就是一个盒子用来装内容

特点：

+ `<div>`标签用来布局，一行只能放一个
+ `<span>`标签用来布局，一行可以放很多个

```html
<div>我是div独占一行</div>
<span>我可以横着显示</span>
<span>我可以横着显示</span>
<span>我可以横着显示</span>
```

### 水平线标签

```html
<hr />
```



## 图像标签

在html标签中，`<img>`标签用于定义html页面中的图像

src是`<img>`的必须属性，它用于指定图像文件的路径和文件名

图像标签属性注意点：

+ 图像属性可以拥有多个属性，必写在标签名的后面
+ 属性间部分先后顺序，标签与与属性之间均以空格分开
+ 属性采取键值对的格式，即`key="value"`的格式，属性="属性值"

```html
<img src="图像url" />
```

图像标签的其他属性：

|        |          |                                    |
| ------ | -------- | ---------------------------------- |
| src    | 图片路径 | 必须属性                           |
| alt    | 文本     | 替换文本，图像不能显示的文字       |
| title  | 文本     | 提示文本，鼠标放在图片上显示的文字 |
| width  | 像素     | 设置图片的宽度                     |
| height | 像素     | 设置图片的高度                     |
| border | 像素     | 设置图片的边框粗细                 |

### 图像标签的使用

```html
<img src="/img/图片.png" />
```

alt 替换文本 图像显示不出来用文字代替

```html
<img src="/img/图片1.png" alt="替换文字" />
```

title 提示文本 鼠标放在图像上提示的文字

```html
<img src="/img/图片.png" alt="替换文字" title="这是一个提示文字"/>
```

width 是给图像设置宽度

```html
<img src="/img/图片.png" alt="替换文字" title="提示文字" width="200"/>
```

height 是给图像设置高度

```html
<ing src="/img/图片.png" alt="提示文字" title="提示文 字" windth="200" height="300"/>
```

border 给图像设置边框粗细

```html
<ing src="/img/图片.png" alt="提示文字" title="提示文 字" windth="200" height="300" border="4" />
```

## 路径标签

路径可分为：

+ 相对路径

相对路径：以引用文件所在位置为参考基础，而建立出的目录路径。

  相对路径分类   符号   说明

  同一级路径        图像文件位于html文件同一级如`<img src="img.png">`

  下一级路径    /    图像文件位于html文件下一级如`<img src="img/img.png">`

  上一级路径    ../   图像文件位于html文件上一级如`img src="../img.png">`

- 绝对路径

绝对路径：是指目录下的绝对位置，直接到达目标位置，通常是从盘符开始的路径。

  例如：`"E:\blog\img\logo.png"`或完整的网络地址：`"https://c2.im5i.com/2022/09/14/5aEG2.png"`

## 超链接标签

在html标签中,`<a>`标签用于定义超链接，作用是从一个页面链接连接到另一个页面

链接的语法格式：

```html
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>
```

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| hter   | 用于指定链接目标的url标签（必须属性）当为标签用于href属性时就具有了超链接的 |
| target | 用于指定链接页面的打开方式，_self为默认值（当前窗口打开）， _blank为在新窗口中打开 |

### 链接的分类

**外部标签：**

```html
<a href="https://yyttm,github,io/">博客</a>
```

**内部标签：**

网站内不页面的相互链接，直接链接内部页面的名称即可

```html
<a href="示例.html">示例</a>
```

**空连接：**

如果但是没有确定的链接目标时

```html
<a href="#">空连接</a>
```

**下载链接：**

如果href里面地址是一个文件或者压缩包会下载这个文件

**网页元素链接：**

在网页中各种网页元素，如文本、图像、表格、音频、视频等都可以添加超链接

**锚点链接**

当我们点击链接，可以快速定位到页面的某个位置，在链接文本的href属性中，设置属性值为#名字的形式，如`<a href="#live">"演艺经历"< /a>`找到目标位置标签里面添加一个id属性=刚才的名字如`<h3id-"live">演艺经历</h3>`

## 注释和特殊字符

如果需要在html文档中添加一些便于阅读和理解单又不需要在页面中注释文字，就需要用注释HTML注释以"`<!--开头，以-->`结束

快捷键：ctrl+/

注释不会显示在网页中，添加注释是为了更好的理解代码的功能，便于相关开发人员理解和阅读代码

## 特殊代码

在html网页中，一些特殊的字符很难或很不方便直接使用，此时我们可以用特殊字符来代替

| 特殊字符 | 描述     | 字符的代码 |
| -------- | -------- | ---------- |
|          | 空格符   | &nbsp；    |
| <        | 小于符   | &lt；      |
| >        | 大于号   | &gt；      |
| &        | 和号     | &amp；     |
| ￥       | 人民币   | &yen；     |
| ©        | 版权     | &copy；    |
| ®        | 注册商标 | &reg；     |
| °        | 摄氏度   | &deg；     |
| ±        | 正负号   | &plusmn；  |
| ×        | 乘号     | &times；   |
| ÷        | 除号     | &divide；  |
| ²        | 平方2    | &sup2；    |
| ³        | 平方3    | &sup3；    |

# 表格标签

表格标签是实际开发中非常常用的标签

表格主要用于显示、展示数据因为它可以让数据显示的非常规整，可读性非常好，特别是后台展示数据的时候，能够熟练运用表格就显得尤为重要，一个清爽简约的表格能够把繁杂的数据表现得很有条理

## 表格的基本语法

```html
<table>
    <tr>
        <td>单元格内的文字</td>
        ...
    </tr>
    ...
</table>
```

<table></table>是用于定义表格的标签
- `<tr></tr>`标签用于定义表格中的行，必须嵌套在`<table>- </table>`标签中。
- `<td></td>`用于定义表格中的单元格，必须嵌套在`<tr></tr>`标签中
- 字母td指表格数据，即数据单元格的内容。

示例

```html
<table>
    <tr><td>姓名</td>   <td>性别</td>   <td>年龄</td></tr>
    <tr><td>小明</td>   <td>男</td>     <td>17</td></tr>
    <tr><td>小兰</td>   <td>女</td>     <td>17</td></tr>
</table>
```

## 表头单元格标签

一般表头单元格位于表格的第一行或第一列，表示单元格里面的文本内容加粗居中显示`<tr>`标签表示html单元格的表头部分

```html
<table>
    <tr>
        <th>姓名</th>
        ...
    <tr>
    ...
</table>
```

示例

```html
<table>
        <th>姓名</th>   <th>性别</th>   <th>年龄</th>
        <tr><td>王小明</td>   <td>男</td> <td>12</td></tr>
        <tr><td>马小兰</td>   <td>女</td> <td>12</td></tr>
</table>
```

## 表格属性

表格标签这部分属性开发不常用后面通过css来设置

| 属性名      | 属性值            | 描述                                         |
| ----------- | ----------------- | -------------------------------------------- |
| align       | left,center,right | 规定表格对周围元素的                         |
| border      | 1或""             | 规定表格单元格是否有边框，默认为""表示无边框 |
| cellpadding | 像素值            | 规定单元格边沿是与内容之间的空白默认1像素    |
| cellspacing | 像素值            | 规定单元格之间的空白，默认2像素              |
| width       | 像素值或百分比    | 规定表格的宽度                               |

**这些属性要写到表格标签table里面**

示例

```html
<table align="center" border="1" cellpadding="5" cellspacing="0" width="500">
        <th>姓名</th>   <th>性别</th>   <th>年龄</th>
        <tr><td>王小明</td>   <td>男</td> <td>12</td></tr>
        <tr><td>马小兰</td>   <td>女</td> <td>12</td></tr>
</table>
```

## 表格的结构标签

使用场景：因为表格可能很长为了更好的表示表格的语义，可以将表格分割称表格头部和表格主题两大部分。

在表格标签中，分别使用`<thead>`标签 表格头部区域、`<tbody>`标签 表格的主体区域、这样可以更好的分清表格结构。

1.`<thead> </thead>`:用于定义表格的头部 `<thead>`内部必须有`<tr>`标签。一般是位于第一行

2.`<tbody> </tbody>:`用于定义表格的主体，主要用于放数据本体

3，以上标签都是放在`<table> </table>`标签中

示例

```html
 <table align="center" border="1" cellpadding="4" cellspacing="0" width="600">
   <thead> <!--头部区域-->
    <tr> 
       <th>排名</th>
       <th>关键词</th>
       <th>趋势</th>
       <th>今日搜索</th> 
       <th>最近七天</th> 
       <th>相关链接</th> 
    </tr>
  </thead> <!--头部区域-->
  <tbody>  <!--主体区域-->
    <tr>
       <td>1</td>
       <td>鬼吹灯</td>
       <td><img src="/img/2.png" width="15" height="15"></td>
       <td>444</td>
       <td>123123</td>
       <td>
           <a href="https://jump2.bdimg.com/f?kw=%E9%AC%BC%E5%90%B9%E7%81%AF" target="_blank">贴吧</a>
           <a href="https://so1.360tres.com/t018bb64bb261a98dda.jpg" target="_blank">图片</a>
           <a href="https://baike.baidu.com/item/%E9%AC%BC%E5%90%B9%E7%81%AF/10790 "target="_blank">百科</a>
       </td>
    </tr>
    <tr>
       <td>2</td>
       <td>盗墓笔记</td>
       <td><img src="/img/1.png" width="15" height="15"></td>
       <td>333</td>
       <td>123122</td>
       <td>
           <a href="https://jump2.bdimg.com/f?kw=%E7%9B%97%E5%A2%93%E7%AC%94%E8%AE%B0&ie=utf-8&tab=good" target="_blank">贴吧</a>
           <a href="https://img.zcool.cn/community/01cf7e5825aa49a84a0e282bae2f1b.jpg?x-oss-process=image/auto-orient,1/resize,m_lfit,w_1280,limit_1/sharpen,100/format,webp/quality,q_100" target="_blank">图片</a>
           <a href="https://baike.baidu.com/item/%E7%9B%97%E5%A2%93%E7%AC%94%E8%AE%B0/21859" target="_blank">百科</a>
       </td>
    </tr>
    <td>3</td>
    <td>西游记</td>
    <td><img src="/img/2.png" width="15" height="15"></td>
    <td>222</td>
    <td>123121</td>
    <td>
        <a href="https://tieba.baidu.com/f?kw=%E8%A5%BF%E6%B8%B8%E8%AE%B0&ie=utf-8" target="_blank">贴吧</a>
        <a href="https://tse1-mm.cn.bing.net/th/id/OIP-C.f4PVD88oV2fpEeoMo2zSAgHaE7?pid=ImgDet&rs=1" target="_blank">图片</a>
        <a href="https://baike.baidu.com/item/%E8%A5%BF%E6%B8%B8%E8%AE%B0/5723" target="_blank">百科</a>
    </td>
 </tr>
</tbody> <!--主体区域-->

    </table>
```

## 合并单元格

特殊情况下，可以把多个单元格合并为一个单元格

1.合并单元格方式

  跨行合并：`rowspan="合并单元格的个数"`

  跨列合并：`colspan="合并单元格的个数"`

2.目标单元格（写合并代码）

  跨行：最上侧单元格为目标单元格，写合并代码

  跨列；最左侧单元格为目标单元格，写合并代码

3.合并单元格的步骤

  合并单元格三部曲

  先确定是跨行还是跨列合并

  找到目标单元格，写上合并方式=合并单元格数量。如`<tdcolspan="2"></td>`

  删除多余的单元格

示例

```html
 <table align="center" border="1" cellpadding="12" cellspacing="0" width=600">
    <tr>
        <td>#</td>
        <td colspan="2">#</td>
        
    </tr>
    <tr>
        <td rowspan="2">#</td>
        <td>#</td>
        <td>#</td>
    </tr>
    <tr>
        
        <td>#</td>
        <td>#</td>
    </tr>

 </table>
```

