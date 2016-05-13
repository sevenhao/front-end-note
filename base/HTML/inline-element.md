###内联元素

* [a](#a)
* [img](#img)
* [input](#input)
* [label](#label)
* [select](#select)
* [span](#span)
* [textarea](#textarea)
* [font](#font)
* [上标sub和下标sup](#sub)
* [HTML 文本格式化 code、em、strong、site](#big)


###<a name="a">a</a>
<div>
<h2>实例</h2>

<p>指向 w3school 的超链接：</p>

<pre>&lt;a href="http://www.w3school.com.cn"&gt;W3School&lt;/a&gt;</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_a)

<div>
<h2>定义和用法</h2>

<p>&lt;a&gt; 标签定义超链接，用于从一张页面链接到另一张页面。</p>

<p>&lt;a&gt; 元素最重要的属性是 href 属性，它指示链接的目标。</p>

<p>在所有浏览器中，链接的默认外观是：</p>

<ul>
<li style="text-decoration: underline; color:#0000ff;">未被访问的链接带有下划线而且是蓝色的</li>
<li style="text-decoration: underline; color:purple;">已被访问的链接带有下划线而且是紫色的</li>
<li style="text-decoration: underline; color:red;">活动链接带有下划线而且是红色的</li>
</ul>
</div>

<div>
<p class="note"><span style="color:blue;">New</span> : HTML5 中的新属性。</p>

<table class="dataintable">
<tbody><tr>
<th style="width:20%;">属性</th>
<th>值</th>
<th>描述</th>
</tr>

<tr>
<td><a href="/tags/att_a_charset.asp" title="HTML <a> 标签的 charset 属性">charset</a></td>
<td><i>char_encoding</i></td>
<td><span class="marked">HTML5 中不支持。</span>规定被链接文档的字符集。</td>
</tr>

<tr>
<td><a href="/tags/att_a_coords.asp" title="HTML <a> 标签的 coords 属性">coords</a></td>
<td><i>coordinates</i></td>
<td><span class="marked">HTML5 中不支持。</span>规定链接的坐标。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_a_download.asp" title="HTML5 <a> download 属性">download</a></td>
<td><i>filename</i></td>
<td>规定被下载的超链接目标。</td>
</tr>

<tr>
<td><a href="/tags/att_a_href.asp" title="HTML <a> 标签的 href 属性">href</a></td>
<td><i>URL</i></td>
<td>规定链接指向的页面的 URL。</td>
</tr>

<tr>
<td><a href="/tags/att_a_hreflang.asp" title="HTML <a> 标签的 hreflang 属性">hreflang</a></td>
<td><i>language_code</i></td>
<td>规定被链接文档的语言。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_a_media.asp" title="HTML5 <a> media 属性">media</a></td>
<td><i>media_query</i></td>
<td>规定被链接文档是为何种媒介/设备优化的。</td>
</tr>

<tr>
<td><a href="/tags/att_a_name.asp" title="HTML <a> 标签的 name 属性">name</a></td>
<td><i>section_name</i></td>
<td><span class="marked">HTML5 中不支持。</span>规定锚的名称。</td>
</tr>

<tr>
<td><a href="/tags/att_a_rel.asp" title="HTML <a> 标签的 rel 属性">rel</a></td>
<td><i>text</i></td>
<td>规定当前文档与被链接文档之间的关系。</td>
</tr>

<tr>
<td><a href="/tags/att_a_rev.asp" title="HTML <a> 标签的 rev 属性">rev</a></td>
<td><i>text</i></td>
<td><span class="marked">HTML5 中不支持。</span>规定被链接文档与当前文档之间的关系。</td>
</tr>

<tr>
<td><a href="/tags/att_a_shape.asp" title="HTML <a> 标签的 shape 属性">shape</a></td>
<td>
	<ul>
	<li>default</li>
	<li>rect</li>
	<li>circle</li>
	<li>poly</li>
	</ul>
</td>
<td><span class="marked">HTML5 中不支持。</span>规定链接的形状。</td>
</tr>

<tr>
<td><a href="/tags/att_a_target.asp" title="HTML <a> 标签的 target 属性">target</a></td>
<td>
	<ul>
	<li>_blank</li>
	<li>_parent</li>
	<li>_self</li>
	<li>_top</li>
	<li><i>framename</i></li>
	</ul>
</td>
<td>规定在何处打开链接文档。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_a_type.asp" title="HTML5 <a> type 属性">type</a></td>
<td><i>MIME type</i></td>
<td>规定被链接文档的的 MIME 类型。</td>
</tr>
</tbody></table>
</div>


###<a name="img">img</a>
<div>
<h2>实例</h2>

<p>在下面的例子中，我们在页面中插入一幅 W3School 的工程师在上海鲜花港拍摄的郁金香照片：</p>
<pre>&lt;img <code>src="/i/eg_tulip.jpg"</code>  alt="上海鲜花港 - 郁金香" /&gt;</pre>

<p>以上代码的效果：</p>
<img src="http://www.w3school.com.cn/i/eg_tulip.jpg" alt="上海鲜花港 - 郁金香">
</div>



###<a name="input">input</a>

<div>
<h2>实例</h2>

<p>一个简单的 HTML 表单，包含两个文本输入框和一个提交按钮：</p>

<pre>&lt;form action="form_action.asp" method="get"&gt;
  First name: <code>&lt;input type="text" name="fname" /&gt;</code>
  Last name: <code>&lt;input type="text" name="lname" /&gt;</code>
  <code>&lt;input type="submit" value="Submit" /&gt;</code>
&lt;/form&gt;
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_form_submit)

<div>
<h2>定义和用法</h2>

<p>&lt;input&gt; 标签用于搜集用户信息。</p>

<p>根据不同的 type 属性值，输入字段拥有很多种形式。输入字段可以是文本字段、复选框、掩码后的文本控件、单选按钮、按钮等等。</p>
</div>


###<a name="label">label</a>
<div>
<h2>实例</h2>

<p>带有两个输入字段和相关标记的简单 HTML 表单：</p>

<pre>&lt;form&gt;
  <code>&lt;label for="male"&gt;Male&lt;/label&gt;</code>
  &lt;input type="radio" name="sex" id="male" /&gt;
  &lt;br /&gt;
  <code>&lt;label for="female"&gt;Female&lt;/label&gt;</code>
  &lt;input type="radio" name="sex" id="female" /&gt;
&lt;/form&gt;
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_label)

<div>
<h2>定义和用法</h2>

<p>&lt;label&gt; 标签为 input 元素定义标注（标记）。</p>

<p>label 元素不会向用户呈现任何特殊效果。不过，它为鼠标用户改进了可用性。如果您在 label 元素内点击文本，就会触发此控件。就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。</p>

<p>&lt;label&gt; 标签的 for 属性应当与相关元素的 id 属性相同。</p>
</div>

###<a name="select">select</a>
<div>
<h2>实例</h2>

<p>创建带有 4 个选项的选择列表：</p>

<pre><code>&lt;select&gt;</code>
  &lt;option value ="volvo"&gt;Volvo&lt;/option&gt;
  &lt;option value ="saab"&gt;Saab&lt;/option&gt;
  &lt;option value="opel"&gt;Opel&lt;/option&gt;
  &lt;option value="audi"&gt;Audi&lt;/option&gt;
<code>&lt;/select&gt;</code>
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_select)

<div>
<h2>属性</h2>

<p class="html5_new_note"><span>New:</span> HTML5 中的新属性。</p>

<table class="dataintable">
<tbody><tr>
<th style="width:20%;">属性</th>
<th style="width:20%;">值</th>
<th style="width:60%;">描述</th>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_select_autofocus.asp" title="HTML <select> 标签的 autofocus 属性">autofocus</a></td>
<td>autofocus</td>
<td>规定在页面加载后文本区域自动获得焦点。</td>
</tr>

<tr>
<td><a href="/tags/att_select_disabled.asp" title="HTML <select> 标签的 disabled 属性">disabled</a></td>
<td>disabled</td>
<td>规定禁用该下拉列表。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_select_form.asp" title="HTML <select> 标签的 form 属性">form</a></td>
<td><i>form_id</i></td>
<td>规定文本区域所属的一个或多个表单。</td>
</tr>

<tr>
<td><a href="/tags/att_select_multiple.asp" title="HTML <select> 标签的 multiple 属性">multiple</a></td>
<td>multiple</td>
<td>规定可选择多个选项。</td>
</tr>

<tr>
<td><a href="/tags/att_select_name.asp" title="HTML <select> 标签的 name 属性">name</a></td>
<td><i>name</i></td>
<td>规定下拉列表的名称。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_select_required.asp" title="HTML <select> 标签的 required 属性">required</a></td>
<td>required</td>
<td>规定文本区域是必填的。</td>
</tr>

<tr>
<td><a href="/tags/att_select_size.asp" title="HTML <select> 标签的 size 属性">size</a></td>
<td><i>number</i></td>
<td>规定下拉列表中可见选项的数目。</td>
</tr>
</tbody></table>
</div>

###<a name="span">span</a>
<pre>&lt;p&gt;<code>&lt;span&gt;some text.&lt;/span&gt;</code>some other text.&lt;/p&gt;</pre>

<p>如果不对 span 应用样式，那么 span 元素中的文本与其他文本不会任何视觉上的差异。尽管如此，上例中的 span 元素仍然为 p 元素增加了额外的结构。</p>

<p>可以为 span 应用 id 或 class 属性，这样既可以增加适当的语义，又便于对 span 应用样式。</p>

###<a name="textarea">textarea</a>
<div>
<h2>实例</h2>

<pre>&lt;textarea rows="3" cols="20"&gt;
在w3school，你可以找到你所需要的所有的网站建设教程。
&lt;/textarea&gt;
</pre>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=demo_html_textarea)

<div>
<h2>定义和用法</h2>

<p>&lt;textarea&gt; 标签定义多行的文本输入控件。</p>

<p>文本区中可容纳无限数量的文本，其中的文本的默认字体是等宽字体（通常是 Courier）。</p>

<p>可以通过 cols 和 rows 属性来规定 textarea 的尺寸，不过更好的办法是使用 CSS 的 height 和 width 属性。</p>

<p class="note"><span>注释：</span>在文本输入区内的文本行间，用 "%OD%OA" （回车/换行）进行分隔。</p>

<p class="tip"><span>提示：</span>可以通过 &lt;textarea&gt; 标签的 wrap 属性设置文本输入区内的换行模式。<a href="/tags/tag_textarea_prop_wrap.asp">有关 wrap 属性的详细信息</a>。</p>
</div>

<div>
<h2>属性</h2>

<p class="html5_new_note"><span>New:</span> HTML5 中的新属性。</p>

<table class="dataintable">
<tbody><tr>
<th style="width:25%;">属性</th>
<th style="width:25%;">值</th>
<th style="width:50%;">描述</th>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_textarea_autofocus.asp" title="HTML <textarea> 标签的 autofocus 属性">autofocus</a></td>
<td>autofocus</td>
<td>规定在页面加载后文本区域自动获得焦点。</td>
</tr>

<tr>
<td><a href="/tags/att_textarea_cols.asp" title="HTML <textarea> 标签的 cols 属性">cols</a></td>
<td><i>number</i></td>
<td>规定文本区内的可见宽度。</td>
</tr>

<tr>
<td><a href="/tags/att_textarea_disabled.asp" title="HTML <textarea> 标签的 disabled 属性">disabled</a></td>
<td>disabled</td>
<td>规定禁用该文本区。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_textarea_form.asp" title="HTML <textarea> 标签的 form 属性">form</a></td>
<td><i>form_id</i></td>
<td>规定文本区域所属的一个或多个表单。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_textarea_maxlength.asp" title="HTML <textarea> 标签的 maxlength 属性">maxlength</a></td>
<td><i>number</i></td>
<td>规定文本区域的最大字符数。</td>
</tr>

<tr>
<td><a href="/tags/att_textarea_name.asp" title="HTML <textarea> 标签的 name 属性">name</a></td>
<td><i>name_of_textarea</i></td>
<td>规定文本区的名称。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_textarea_placeholder.asp" title="HTML <textarea> 标签的 placeholder 属性">placeholder</a></td>
<td><i>text</i></td>
<td>规定描述文本区域预期值的简短提示。</td>
</tr>

<tr>
<td><a href="/tags/att_textarea_readonly.asp" title="HTML <textarea> 标签的 readonly 属性">readonly</a></td>
<td>readonly</td>
<td>规定文本区为只读。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_textarea_required.asp" title="HTML <textarea> 标签的 required 属性">required</a></td>
<td>required</td>
<td>规定文本区域是必填的。</td>
</tr>

<tr>
<td><a href="/tags/att_textarea_rows.asp" title="HTML <textarea> 标签的 rows 属性">rows</a></td>
<td><i>number</i></td>
<td>规定文本区内的可见行数。</td>
</tr>

<tr>
<td class="html5_new"><a href="/tags/att_textarea_wrap.asp" title="HTML <textarea> 标签的 wrap 属性">wrap</a></td>
<td>
    <ul>
    <li>hard</li>
    <li>soft</li>
    </ul>
</td>
<td>规定当在表单中提交时，文本区域中的文本如何换行。。</td>
</tr>

</tbody></table>
</div>


###<a name="font">font</a>
<div>
<h2>实例</h2>

<p>规定文本字体、大小和颜色：</p>

<pre><code>&lt;font size="3" color="red"&gt;</code>This is some text!<code>&lt;/font&gt;</code>
<code>&lt;font size="2" color="blue"&gt;</code>This is some text!<code>&lt;/font&gt;</code>
<code>&lt;font face="verdana" color="green"&gt;</code>This is some text!<code>&lt;/font&gt;</code>
</pre>

<p class="tiy"><a target="_blank" href="/tiy/t.asp?f=html_font">亲自试一试</a></p>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_font)


###<a name="sub">上标sub和下标sup</a>

<pre>
<code>
&lt;p&gt;
This text contains &lt;sub&gt;subscript&lt;/sub&gt;
&lt;/p&gt;

&lt;p&gt;
This text contains &lt;sup&gt;superscript&lt;/sup&gt;
&lt;/p&gt;
</code>
</pre>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_sup)


###<a name="big">HTML 文本格式化</a>
<div>
<h2>定义和用法</h2>
<p><strong>以下元素都是短语元素。虽然这些标签定义的文本大多会呈现出特殊的样式，但实际上，这些标签都拥有确切的语义。</strong></p>
<p><strong>我们并不反对使用它们，但是如果您只是为了达到某种视觉效果而使用这些标签的话，我们建议您使用样式表，那么做会达到更加丰富的效果。</strong></p>
<table class="dataintable">
<tbody><tr>
<td><a href="/tags/tag_em.asp" title="HTML <em> 标签">&lt;em&gt;</a></td>
<td>把文本定义为强调的内容。</td>
</tr>

<tr>
<td><a href="/tags/tag_strong.asp" title="HTML <strong> 标签">&lt;strong&gt;</a></td>
<td>把文本定义为语气<em>更强</em>的强调的内容。</td>
</tr>

<tr>
<td><a href="/tags/tag_dfn.asp" title="HTML <dfn> 标签">&lt;dfn&gt;</a></td>
<td>定义一个定义项目。</td>
</tr>

<tr>
<td><a href="/tags/tag_code.asp" title="HTML <code> 标签">&lt;code&gt;</a></td>
<td>定义计算机代码文本。</td>
</tr>

<tr>
<td><a href="/tags/tag_samp.asp" title="HTML <samp> 标签">&lt;samp&gt;</a></td>
<td>定义样本文本。</td>
</tr>

<tr>
<td><a href="/tags/tag_kbd.asp" title="HTML <kbd> 标签">&lt;kbd&gt;</a></td>
<td>定义键盘文本。它表示文本是从键盘上键入的。它经常用在与计算机相关的文档或手册中。</td>
</tr>

<tr>
<td><a href="/tags/tag_var.asp" title="HTML <var> 标签">&lt;var&gt;</a></td>
<td>定义变量。您可以将此标签与 &lt;pre&gt; 及 &lt;code&gt; 标签配合使用。</td>
</tr>

<tr>
<td><a href="/tags/tag_cite.asp" title="HTML <cite> 标签">&lt;cite&gt;</a></td>
<td>定义引用。可使用该标签对参考文献的引用进行定义，比如书籍或杂志的标题。</td>
</tr>
</tbody></table>
</div>

[显示效果](http://www.w3school.com.cn/tiy/t.asp?f=html_textformatting)


更多详情请参考[《HTML参考手册》——标签](http://www.w3school.com.cn/tags/index.asp)

