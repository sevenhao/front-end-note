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

###<a name="address">address</a>
<pre>&lt;address&gt;
Written by &lt;a href="mailto:webmaster@example.com"&gt;Donald Duck&lt;/a&gt;.&lt;br&gt; 
Visit us at:&lt;br&gt;
Example.com&lt;br&gt;
Box 564, Disneyland&lt;br&gt;
USA
&lt;/address&gt;
</pre>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_address)

* 用法 
如果 <code>&lt;address&gt;</code> 元素位于<code>&lt;body&gt;</code> 元素内，则它表示文档联系信息。
如果<code>&lt;address&gt;</code> 元素位于 <code>&lt;article&gt;</code>  元素内，则它表示文章的联系信息。
<code>&lt;address&gt;</code>  元素中的文本通常呈现为斜体。

###<a name="div">div</a>
<pre><code>&lt;div <span style="color:red;">style="color:#00FF00"</span>&gt;</code>
  &lt;h3&gt;This is a header&lt;/h3&gt;
  &lt;p&gt;This is a paragraph.&lt;/p&gt;
<code>&lt;/div&gt;</code>
</pre>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_div_test)

* 用法 
<code>&lt;div&gt;</code>是一个块级元素。这意味着它的内容自动地开始一个新行。实际上，换行是<code>&lt;div&gt;</code>固有的唯一格式表现。可以通过 <code>&lt;div&gt;</code>的 class 或 id 应用额外的样式。


###dl

<div>
<h2>实例</h2>

<pre><code>&lt;dl&gt;</code>
   &lt;dt&gt;计算机&lt;/dt&gt;
   &lt;dd&gt;用来计算的仪器 ... ...&lt;/dd&gt;
   &lt;dt&gt;显示器&lt;/dt&gt;
   &lt;dd&gt;以视觉方式显示信息的装置 ... ...&lt;/dd&gt;
<code>&lt;/dl&gt;</code>
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_list_definition)


###fieldse
<div>
<h2>实例</h2>

<p>组合表单中的相关元素：</p>

<pre>&lt;form&gt;
  <code>&lt;fieldset&gt;</code>
    &lt;legend&gt;health information&lt;/legend&gt;
    height: &lt;input type="text" /&gt;
    weight: &lt;input type="text" /&gt;
  <code>&lt;/fieldset&gt;</code>
&lt;/form&gt;
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_fieldset)

* 用法 
<div>
<p>fieldset 元素可将表单内的相关元素分组。</p>

<p>&lt;fieldset&gt; 标签将表单内容的一部分打包，生成一组相关表单的字段。</p>
<p>当一组表单元素放到 &lt;fieldset&gt; 标签内时，浏览器会以特殊方式来显示它们，它们可能有特殊的边界、3D 效果，或者甚至可创建一个子表单来处理这些元素。</p>

<p>&lt;fieldset&gt; 标签没有必需的或唯一的属性。</p>

<p><a href="/tags/tag_legend.asp" title="HTML <legend> 标签">&lt;legend&gt; 标签</a>为 fieldset 元素定义标题。</p>
</div>


###form 
<div>
<h2>例子</h2>

<pre><code>&lt;form action="form_action.asp" method="get"&gt;</code>
  &lt;p&gt;First name: &lt;input type="text" name="fname" /&gt;&lt;/p&gt;
  &lt;p&gt;Last name: &lt;input type="text" name="lname" /&gt;&lt;/p&gt;
  &lt;input type="submit" value="Submit" /&gt;
<code>&lt;/form&gt;</code>
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_form_submit)

* 用法 
<div>
<p>&lt;form&gt; 标签用于为用户输入创建 HTML 表单。</p>

<p>表单能够包含 <a href="/tags/tag_input.asp" title="HTML <input> 标签">input 元素</a>，比如文本字段、复选框、单选框、提交按钮等等。</p>

<p>表单还可以包含 <a href="/tags/tag_menu.asp" title="HTML <menu> 标签">menus</a>、<a href="/tags/tag_textarea.asp" title="HTML <textarea> 标签">textarea</a>、<a href="/tags/tag_fieldset.asp" title="HTML <fieldset> 标签">fieldset</a>、<a href="/tags/tag_legend.asp" title="HTML <legend> 标签">legend</a> 和 <a href="/tags/tag_label.asp" title="HTML <label> 标签">label 元素</a>。</p>

<p>表单用于向服务器传输数据。</p>
</div>

<div>
<h2>属性</h2>

<p class="html5_new_note"><span>new</span>  HTML5 中的新属性。</p>

<table class="dataintable">
  <tbody><tr>
    <th>属性</th>
    <th>值</th>
    <th>描述</th>
  </tr>

  <tr>
    <td>accept</td>
    <td><i>MIME_type</i></td>
    <td><span class="deprecated">HTML 5 中不支持。</span></td>
  </tr>

  <tr>
    <td><a href="/tags/att_form_accept-charset.asp" title="HTML5 <form> accept-charset 属性">accept-charset</a></td>
    <td><i>charset_list</i></td>
    <td>规定服务器可处理的表单数据字符集。</td>
  </tr>

  <tr>
    <td><a href="/tags/att_form_action.asp" title="HTML5 <form> action 属性">action</a></td>
    <td><i>URL</i></td>
    <td>规定当提交表单时向何处发送表单数据。</td>
  </tr>

  <tr>
    <td class="html5_new"><a href="/tags/att_form_autocomplete.asp" title="HTML5 <form> autocomplete 属性">autocomplete</a></td>
    <td>
      <ul>
      <li>on</li>
      <li>off</li>
      </ul>
    </td>
    <td>规定是否启用表单的自动完成功能。</td>
  </tr>

  <tr>
    <td><a href="/tags/att_form_enctype.asp" title="HTML5 <form> enctype 属性">enctype</a></td>
    <td>见说明</td>
    <td>规定在发送表单数据之前如何对其进行编码。</td>
  </tr>

  <tr>
    <td><a href="/tags/att_form_method.asp" title="HTML5 <form> method 属性">method</a></td>
    <td>
      <ul>
      <li>get</li>
      <li>post</li>
      </ul>
    </td>
    <td>规定用于发送 form-data 的 HTTP 方法。</td>
  </tr>

  <tr>
    <td><a href="/tags/att_form_name.asp" title="HTML5 <form> name 属性">name</a></td>
    <td><i>form_name</i></td>
    <td>规定表单的名称。</td>
  </tr>

  <tr>
    <td class="html5_new"><a href="/tags/att_form_novalidate.asp" title="HTML5 <form> novalidate 属性">novalidate</a></td>
    <td>novalidate</td>
    <td>如果使用该属性，则提交表单时不进行验证。</td>
  </tr>

  <tr>
    <td><a href="/tags/att_form_target.asp" title="HTML5 <form> target 属性">target</a></td>
    <td>
      <ul>
      <li>_blank</li>
      <li>_self</li>
      <li>_parent</li>
      <li>_top</li>
      <li><i>framename</i></li>
      </ul>
    </td>
    <td>规定在何处打开 action URL。</td>
  </tr>
</tbody></table>
</div>


###h1 - h6标题
<div>
<h2>实例</h2>

<p>六个不同的 HTML 标题：</p>

<pre>&lt;h1&gt;这是标题 1&lt;/h1&gt;
&lt;h2&gt;这是标题 2&lt;/h2&gt;
&lt;h3&gt;这是标题 3&lt;/h3&gt;
&lt;h4&gt;这是标题 4&lt;/h4&gt;
&lt;h5&gt;这是标题 5&lt;/h5&gt;
&lt;h6&gt;这是标题 6&lt;/h6&gt;
</pre>

<p class="tiy"><a target="_blank" href="/tiy/t.asp?f=html_headers">亲自试一试</a></p>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_headers)

###hr
<div>
<h2>实例</h2>

<p>被水平线分隔的标题和段落：</p>

<pre>&lt;h1&gt;This is header 1&lt;/h1&gt;
<code>&lt;hr /&gt;</code>
&lt;p&gt;This is some text&lt;/p&gt;
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_hr)


###ol - 排序表单
<div>
<h2>实例</h2>

<p>有序 HTML 列表：</p>

<pre><code>&lt;ol&gt;</code>
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
<code>&lt;/ol&gt;</code>
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_list_ordered)

<div>
<h2>属性</h2>

<p>New：HTML5 中的新属性。</p>


<table class="dataintable">
<tbody><tr>
<th>属性</th>
<th>值</th>
<th>描述</th>
</tr>

<tr>
<td><a href="/tags/att_ol_compact.asp">compact</a></td>
<td>compact</td>
<td><p>HTML5 中不支持。HTML 4.01 中不赞成使用。</p><p>规定列表呈现的效果比正常情况更小巧。</p></td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_ol_reversed.asp">reversed</a></td>
<td>reversed</td>
<td>规定列表顺序为降序。(9,8,7...)</td>
</tr>

<tr>
<td><a href="/tags/att_ol_start.asp">start</a></td>
<td><i>number</i></td>
<td>规定有序列表的起始值。</td>
</tr>

<tr>
<td><a href="/tags/att_ol_type.asp">type</a></td>
<td>
    <ul>
    <li>1</li>
    <li>A</li>
    <li>a</li>
    <li>I</li>
    <li>i</li>
    </ul>
</td>
<td>规定在列表中使用的标记类型。</td>
</tr>
</tbody></table>
</div>


###table - 表格
<div>
<h2>实例</h2>

<p>一个简单的 HTML 表格，包含两行两列：</p>

<pre><code>&lt;table border="1"&gt;</code>
  &lt;tr&gt;
    &lt;th&gt;Month&lt;/th&gt;
    &lt;th&gt;Savings&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;January&lt;/td&gt;
    &lt;td&gt;$100&lt;/td&gt;
  &lt;/tr&gt;
<code>&lt;/table&gt;</code>
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_table_test)


### ul - 非排序列表
<div>
<h2>实例</h2>

<p>无序 HTML 列表：</p>

<pre><code>&lt;ul&gt;</code>
  &lt;li&gt;Coffee&lt;/li&gt;
  &lt;li&gt;Tea&lt;/li&gt;
  &lt;li&gt;Milk&lt;/li&gt;
<code>&lt;/ul&gt;</code>
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_list_unordered)
