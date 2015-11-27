# HTML常用元素介绍

## 目录
* [基础标签](#base)
* [元素](#tag)
* [属性](#property)
* [块级元素](#block)


## <a name="base">基础标签</a>
<ul>
<li>&lt;html&gt; 与 &lt;/html&gt; 之间的文本描述网页</li>
<li>&lt;body&gt; 与 &lt;/body&gt; 之间的文本是可见的页面内容</li>
<li>&lt;h1&gt; 与 &lt;/h1&gt; 之间的文本被显示为标题</li>
<li>&lt;p&gt; 与 &lt;/p&gt; 之间的文本被显示为段落</li>
</ul>

##<a name="tag">元素</a>
HTML 元素指的是从开始标签（start tag）到结束标签（end tag）的所有代码。
<h3>&lt;p&gt; 元素：</h3>
<pre>&lt;p&gt;This is my first paragraph.&lt;/p&gt;</pre>
<p>这个 &lt;p&gt; 元素定义了 HTML 文档中的一个段落。</p>
<p>这个元素拥有一个开始标签 &lt;p&gt;，以及一个结束标签 &lt;/p&gt;。</p>
<p>元素内容是：This is my first paragraph。</p>


##<a name="property">属性</a>
<div>
<h2>HTML 属性</h2>

<p>HTML 标签可以拥有<em>属性</em>。属性提供了有关 HTML 元素的<em>更多的信息</em>。</p>

<p>属性总是以名称/值对的形式出现，比如：<em>name="value"</em>。</p>

<p>属性总是在 HTML 元素的<em>开始标签</em>中规定。</p>
</div>

更多详情请参考[<《HTML参考手册》——属性](http://www.w3school.com.cn/tags/html_ref_standardattributes.asp)


##<a name="block">块级元素</a>
* 块元素一般都从新行开始，它可以容纳内联元素和其他块元素,常见块元素是段落标签'P"。“form"这个块元素比较特殊，它只能用来容纳其他块元素。
* 如果没有css的作用，块元素会顺序以每次另起一行的方式一直往下排。而有了css以后，我们可以改变这种html的默认布局模式，把块元素摆放到你想要 的位置上去。


* <h2>块元素(block element)</h2>   
<table>
    <tbody>
    <tr>
        <td>元素</td>
        <td>描述</td>
        <td>元素</td>
        <td>描述</td>
    </tr>
    <tr>
        <td>address</td>
        <td>地址:文档或文章的作者/拥有者的联系信息。</td>
        <td>blockquote</td>
        <td>块引用</td>
    </tr>
    <tr>
        <td>form</td>
        <td>交互表单</td>
        <td>center </td>
        <td>地址:文档或文章的作者/拥有者的联系信息。</td>
    </tr>
    <tr>
        <td>dl</td>
        <td>定义列表</td>
        <td>div</td>
        <td>常用块级容器，定义文档中的分区或节。标签可以把文档分割为独立的、不同的部分。</td>
    </tr>
    <tr>
        <td>fieldset</td>
        <td>form控制组</td>
        <td>dir</td>
        <td>目录列表。<em>提示</em>不赞成使用 dir 元素！</td>
    </tr>
    <tr>
        <td>h1</td>
        <td>大标题</td>
        <td>h2</td>
        <td>副标题</td>
    </tr>
    <tr>
        <td>h3</td>
        <td>3级标题</td>
        <td>h4</td>
        <td>4级标题</td>
    </tr>
    <tr>
        <td>h5</td>
        <td>5级标题</td>
        <td>h6</td>
        <td>6级标题</td>
    </tr>
    <tr>
        <td>hr</td>
        <td>水平分隔线</td>
        <td>isindex</td>
        <td>input prompt</td>
    </tr>
    <tr>
        <td>menu</td>
        <td>菜单列表</td>
        <td>noframes</td>
        <td>frames可选内容，（对于不支持frame的浏览器显示此区块内容</td>
    </tr>
    <tr>
        <td>ol</td>
        <td>排序表单</td>
        <td>noscript</td>
        <td>可选脚本内容（对于不支持script的浏览器显示此内容）</td>
    </tr>
    <tr>
        <td>p</td>
        <td>段落</td>
        <td>pre</td>
        <td>格式化文本</td>
    </tr>
    <tr>
        <td>table</td>
        <td>表格</td>
        <td>ul</td>
        <td>非排序列表</td>
    </tr>
    </tbody>
</table>

####[常用块级元素详情](https://github.com/sevenhao/front-end-note/blob/master/base/HTML/block-tag.md)


##<a name="block">内联元素(inline element)</a>
* 内联元素(inline element)一般都是基于语义级(semantic)的基本元素。
* 内联元素只能容纳文本或者其他内联元素，常见内联元素 “a”。

* <h2>内联元素(inline element)<</h2>
<table>
    <tbody>
    <tr>
        <td>元素</td>
        <td>描述</td>
        <td>元素</td>
        <td>描述</td>
    </tr>
    <tr>
        <td>a</td>
        <td>标签定义超链接，用于从一张页面链接到另一张页面。</td>
        <td>u</td>
        <td>下划线</td>
    </tr>
    <tr>
        <td>acronym </td>
        <td>标签定义首字母缩写。
            <span class="marked">HTML5 中不支持 &lt;acronym&gt; 标签。请使用
                &lt;abbr&gt;代替。</span></td>
        <td>br</td>
        <td>换行</td>
    </tr>
    <tr>
        <td>bdo </td>
        <td>元素可覆盖默认的文本方向。</td>
        <td>big </td>
        <td>标签呈现大号字体效果。</td>
    </tr>
    <tr>
        <td>b</td>
        <td>标签规定粗体文本</td>
        <td>img </td>
        <td>图片</td>
    </tr>
    <tr>
        <td>code </td>
        <td>计算机代码(在引用源码的时候需要)</td>
        <td>dfn </td>
        <td>定义字段</td>
    </tr>
    <tr>
        <td>em </td>
        <td>强调</td>
        <td>font </td>
        <td>规定文本的字体、字体尺寸、字体颜色。</td>
    </tr>
    <tr>
        <td>i</td>
        <td>斜体</td>
        <td>cite </td>
        <td>它所包含的文本对某个参考文献的引用，比如书籍或者杂志的标题。</td>
        
    </tr>
    <tr>
        <td>input </td>
        <td>输入框</td>
        <td>kbd </td>
        <td>定义键盘文本</td>
    </tr>
    <tr>
        <td>label</td>
        <td>标签为 input 元素定义标注（标记）</td>
        <td>q</td>
        <td>短引用 </td>
    </tr>
    <tr>
        <td>select </td>
        <td>元素可创建单选或多选菜单</td>
        <td>small </td>
        <td>小字体文本   </td>
    </tr>
    <tr>
        <td>span</td>
        <td>常用内联容器，定义文本内区块</td>
        <td>strike </td>
        <td>中划线，删除线</td>
    </tr>
    <tr>
        <td>strong </td>
        <td>粗体强调</td>
        <td>sub</td>
        <td>下标</td>
    </tr>
    <tr>
        <td>sup </td>
        <td>上标</td>
        <td>textarea</td>
        <td>多行文本输入框</td>
    </tr>
    <tr>
        <td>tt</td>
        <td>电传文本</td>
        <td>abbr </td>
        <td>标签指示简称或缩写，比如 "WWW" 或 "NATO"。</td>
    </tr>
    </tbody>
</table>

####[常用内联元素详情](https://github.com/sevenhao/front-end-note/blob/master/base/HTML/inline-element.md)

