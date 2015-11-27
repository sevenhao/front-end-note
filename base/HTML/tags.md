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
        <td>center </td>
        <td>地址:文档或文章的作者/拥有者的联系信息。</td>
        <td>dir</td>
        <td>目录列表。<em>提示</em>不赞成使用 dir 元素！</td>
    </tr>
    <tr>
        <td>div</td>
        <td>常用块级容器，定义文档中的分区或节。标签可以把文档分割为独立的、不同的部分。</td>
        <td>dl</td>
        <td>定义列表</td>
        
    </tr>
    <tr>
        <td>fieldset</td>
        <td>form控制组</td>
        <td>form</td>
        <td>交互表单</td>
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
        <td>noscript</td>
        <td>可选脚本内容（对于不支持script的浏览器显示此内容）</td>
        <td>ol</td>
        <td>排序表单</td>
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

###<a name="address">address</a>

* address - 地址:文档或文章的作者/拥有者的联系信息。
* blockquote - 块引用。
* center - 举中对齐块。<em>提示</em>：请使用 CSS 样式来居中文本。
* dir - 目录列表。<em>提示</em>不赞成使用 dir 元素！
* div - 常用块级容器，定义文档中的分区或节。标签可以把文档分割为独立的、不同的部分。
* dl - 定义列表
* fieldset - form控制组
* form - 交互表单
* h1 - 大标题
* h2 - 副标题
* h3 - 3级标题
* h4 - 4级标题
* h5 - 5级标题
* h6 - 6级标题
* hr - 水平分隔线
* isindex - input prompt
* menu - 菜单列表
* noframes - frames可选内容，（对于不支持frame的浏览器显示此区块内容
* noscript - 可选脚本内容（对于不支持script的浏览器显示此内容）
* ol - 排序表单
* p- 段落
* pre - 格式化文本
* table - 表格
* ul - 非排序列表

