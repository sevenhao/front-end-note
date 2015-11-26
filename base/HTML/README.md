# HTML

## 目录
* [HTML 介绍](#what)
* [书写方式](#write)
* [基本结构](#struct)
* [头部内容](#head)
* [标签(也叫元素)](#tag)
* [块级元素和行内元素](#block-and-inline)
* [替换元素和非替换元素](#replaced-elements-and-not)
* [字符集](#word)
* [基础知识学习网站](#reading)

## <a name="what">HTML 介绍</a>
* 超文本标记语言。HyperText Markup Language的缩写，
* 多用于网页，用此编写的文件为静态网页，后缀名为：.html或.htm。

## <a name="write">书写方式</a>
* 它其实是文本，它需要浏览器的解释，它的编辑器大体可以分为三种，
  基本文本、文档编辑软件，使用微软自带的记事本或写字板都可以编写，当然，如果你用WPS来编写，也可以。不过存盘时请使用.htm或.html作为扩展名，这样就方便浏览器认出直接解释执行了。
* 半所见即所得软件，
  如：FCK-Editer、E-webediter等在线网页编辑器；
  尤其推荐：Sublime Text代码编辑器（由Jon Skinner开发，Sublime Text）。
* 所见即所得软件，使用最广泛的编辑器，完全可以一点不懂HTML的知识就可以做出网页，如：
  FRONTPAGE（出品单位：微软）；
  Dreamweaver（出品单位：Adobe）。
* 所见即所得软件与半所见即所得的软件相比，开发速度更快，效率更高，且直观的表现更强。任何地方进行修改只需要刷新即可显示。缺点是生成的代码结构复杂，不利于大型网站的多人协作和精准定位等高级功能的实现。


## <a name="struct">基本结构</a>
网页是的一系列的标签组成的。    
例如
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>标题</title>
</head>
<body>
	<h1>My First Heading</h1>
	<p>My first paragraph.</p>
</body>
</html>
```
其中
* DOCTYPE定义了文档类型。`<!DOCTYPE html>`表明这是一个HTML5文档
* `<html>`和`</html>`之间的内容描述了网页
* `<head>`和`</head>`之间的内容描述了网页的一些额外信息。不会被显示
* `<title>`之间的内容描述了网页的标题。会在网页标签上显示
* `<meta charset="utf-8">`让浏览器用utf-8的编码格式来对文档内容进行编码
* `<body>`和`</body>`之间的内容描述网页的可见部分
* `<h1>`和`</h1>`之间的内容描述标题
* `<p>`和`</p>`之间的内容描述了段落

## <a name="struct">头部内容</a> 
```
<head></head>
```
这2个标记符分别表示头部信息的开始和结尾。
头部中包含的标记是页面的标题、序言、说明等内容，它本身不作为内容来显示，但影响网页显示的效果。
头部中最常用的标记符是标题标记符和meta标记符，其中标题标记符用于定义网页的标题，它的内容显示在网页窗口的标题栏中，网页标题可被浏览器用作书签和收藏清单。

<table>
<tbody>
<tr><td><em>标签</em></td><td><em>描述</em></td></tr>
<tr><td>head</td><td>定义了文档的信息</td></tr>
<tr><td>title/td><td>定义了文档的标题</td></tr>
<tr><td>base</td><td>定义了页面链接标签的默认链接地址</td></tr>
<tr><td>link</td><td>定义了一个文档和外部资源之间的关系</td></tr>
<tr><td>meta</td><td>定义了HTML文档中的元数据</td></tr>
<tr><td>script</td><td>定义了客户端的脚本文件</td></tr>
<tr><td>style</td><td>定义了HTML文档的样式文件</td></tr>
</tbody>
</table>

## <a name="what">标签(也叫元素)</a>
标签分为能包含标签内容和不能包含标签内容这两类。    

**能包含内容的标签**由开始标签，结束标签，标签属性，标签的内容组成的。例如：
```
<a href="https://github.com/sevenhao" title="sevenhao">sevenhao</a>
```
其中:    
* `<a href="https://github.com/sevenhao" title="sevenhao">`为起始标签
* `</a>`为结束标签
* `href`和`title`为标签属性，`https://github.com/sevenhao`和`sevenhao`为属性对应的值。属性的值要由英文的双引号包起来。
* `sevenhao`为标签的内容。

**不能包含内容的标签**被称为空元素。空元素是在开始标签中关闭的。    
如 `<br/>`, `<input type="text" />`

###数据类型
* 超文本标记语言定义了多种数据类型的元素内容，如脚本数据和样式表的数据，和众多类型的属性值，包括ID、名称、URI、数字、长度单位、语言、媒体描述符、颜色、字符编码、日期和时间等。所有这些数据类型都是专业的字符数据。

###[常用标签介绍]()


## <a name="block-and-inline">块级元素和行内元素</a>
* 块级元素会始终占居一行，而行内元素并不会。  

* 常见的块级元素有 `div, form, table, header, aside, section, article, figure, figcaption, h1~h6, nav, p, pre, blockqoute, canvas, ol, ul, dl`    

* 常见的行内元素有 `span, a, img, label, input, select, textarea, br, i, em, strong, small, button, sub, sup, code`


## <a name="replaced-elements-and-not">替换元素和非替换元素</a>
* 替换元素就是指浏览器是根据元素的属性来判断具体要显示的内容的元素，比如 img 标签，浏览器是根据其 src 的属性值来读取这个元素所包含的内容的，常见的替换元素还有 input 、textarea、 select、 object、 iframe 和 video 等等，这些元素都有一个共同的特点，就是浏览器并不直接显示其内容，而是通过其某个属性的值来显示具体的内容，比如浏览器会根据 input 中的 type 的属性值来判断到底应该显示单选按钮还是多选按钮亦或是文本输入框。

* 非替换元素，比如 p、label 元素等等，浏览器这是直接显示元素所包含的内容。

## <a name="word">字符集</a>

## <a name="reading">基础知识学习网站</a>
* [w3school](http://www.w3school.com.cn/h.asp)
* [菜鸟教程](http://www.runoob.com/html/html-tutorial.html)
