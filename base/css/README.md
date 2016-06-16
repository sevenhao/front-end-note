# CSS

## 目录
* [CSS 概述](#what)
* [样式表层叠顺序](#turn)
* [基础语法](#base)
* [高级语法](#high)
* [CSS样式](#style)
* [基础知识学习网站](#reading)

## <a name="what">CSS 概述</a>
<div>
<ul>
<li>CSS 指层叠样式表 (<em>C</em>ascading <em>S</em>tyle <em>S</em>heets)</li>
<li>样式定义<em>如何显示</em> HTML 元素</li>
<li>CSS是一门语言<em>（DSL）</em></li>
<li>把样式添加到 HTML 4.0 中，是为了<em>解决内容与表现分离的问题</em></li>
<li><em>外部样式表</em>可以极大提高工作效率</li>
<li>外部样式表通常存储在 <em>CSS 文件</em>中</li>
<li>多个样式定义可<em>层叠</em>为一</li>
</ul>

</div>

## <a name="turn">样式表层叠顺序</a>
<div>
<p>样式表允许以多种方式规定样式信息。样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。</p>

<h3>层叠次序(优先权由高到低)</h3>
<p><strong>当同一个 HTML 元素被不止一个样式定义时，会使用哪个样式呢？</strong></p>
<p>一般而言，所有的样式会根据下面的规则层叠于一个新的虚拟样式表中，其中数字1 拥有最高的优先权。</p>

<ol>
<li>内联样式（在 HTML 元素内部）</li>
<li>内部样式表（位于 &lt;head&gt; 标签内部）</li>
<li>外部样式表</li>
<li>浏览器缺省设置</li>
</ol>
</div>


### 写在标签的`style`属性里
写在标签的`style`属性里的样式称为，称为内联样式。例如
```
<p style="color: sienna; margin-left: 20px">
This is a paragraph
</p>
```

### 写在&lt;head&gt; 的`style`标签内
写在`style`标签内的样式称为内部样式表。例如
```
<style type="text/css">
  hr {color: sienna;}
  p {margin-left: 20px;}
  body {background-image: url("images/back40.gif");}
</style>
```

### 写在一个文件里的样式叫做外部样式表。    
这样的文件的后缀名为`css`。    
例如,`test.css`文件中的内容
```css
hr {color: sienna;}
p {margin-left: 20px;}
body {background-image: url("images/back40.gif");}
```

页面中用外部样式表要用`link`标签，例如
```
<link rel="stylesheet" type="text/css" href="path/to/test.css" />
```
`link`标签要放在`head`标签中。否则页面可能会闪烁。

### 外部样式表，内部样式表，内联样式比较
推荐使用外部样式表。不建议使用内部样式表和内联样式。

原因：
外部样式表    
* 能被复用
* 能被缓存


## <a name="base">基础语法</a>
<div>
<h2>CSS 语法</h2>

<p>CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明。</p>

<pre>selector {declaration1; declaration2; ... declarationN }</pre>

<p>选择器通常是您需要改变样式的 HTML 元素。</p>

<p>每条声明由一个属性和一个值组成。</p>

<p>属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。</p>

<pre>selector {property: value}</pre>

<p>下面这行代码的作用是将 h1 元素内的文字颜色定义为红色，同时将字体大小设置为 14 像素。</p>

<p>在这个例子中，h1 是选择器，color 和 font-size 是属性，red 和 14px 是值。</p>

<pre>h1 {color:red; font-size:14px;}</pre>

<p>下面的示意图为您展示了上面这段代码的结构：</p>

<img src="https://github.com/sevenhao/front-end-note/blob/master/base/css/ct_css_selector.gif" alt="CSS 语法">

<p class="tip"><span>提示：</span>请使用花括号来包围声明。</p>
</div>

## <a name="high">高级语法</a>
<div>
<h2>选择器的分组</h2>
<p>你可以对选择器进行分组，这样，被分组的选择器就可以分享相同的声明。用逗号将需要分组的选择器分开。在下面的例子中，我们对所有的标题元素进行了分组。所有的标题元素都是绿色的。</p>
<pre><code>h1,h2,h3,h4,h5,h6</code> {
  color: green;
  }</pre>
</div>

<div>
<h2>继承及其问题</h2>
<p>根据 CSS，子元素从父元素继承属性。但是它并不总是按此方式工作。看看下面这条规则：</p>
<pre>body {
     font-family: Verdana, sans-serif;
     }</pre>
<p>根据上面这条规则，站点的 body 元素将使用 Verdana 字体（假如访问者的系统中存在该字体的话）。</p>
<p>通过 CSS 继承，子元素将继承最高级元素（在本例中是 body）所拥有的属性（这些子元素诸如 p, td, ul, ol, ul, li, dl, dt,和 dd）。不需要另外的规则，所有 body 的子元素都应该显示 Verdana 字体，子元素的子元素也一样。并且在大部分的现代浏览器中，也确实是这样的。</p>
<p>但是在那个浏览器大战的血腥年代里，这种情况就未必会发生，那时候对标准的支持并不是企业的优先选择。比方说，Netscape 4 就不支持继承，它不仅忽略继承，而且也忽略应用于 body 元素的规则。IE/Windows 直到 IE6 还存在相关的问题，在表格内的字体样式会被忽略。我们又该如何是好呢？</p>
</div>

<h2><a href="https://github.com/sevenhao/front-end-note/blob/master/base/css/inheritance-and-cascade.md">样式继承详细介绍</a></h2>

##<a name="style">CSS样式</a>
* [CSS样式](https://github.com/sevenhao/front-end-note/edit/master/base/css/cssstyle.md)
* [CSS 常见样式示例](https://github.com/sevenhao/front-end-note/blob/master/base/css/cssexample.md)
* [CSS 常见样式问题解决方法](https://github.com/sevenhao/front-end-note/blob/master/base/css/cssfaq.md)
* [transition与visibility延时隐藏]()


## <a name="reading">基础知识学习网站</a>
* [w3school](http://www.w3school.com.cn/css/index.asp)
* [菜鸟教程](http://www.runoob.com/html/html-tutorial.html)
