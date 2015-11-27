###内联元素

* [a](#a)
* [img](#img)
* [input](#input)


###<a name="a">a</a>
<div>
<h2>实例</h2>

<p>指向 w3school 的超链接：</p>

<pre>&lt;a href="http://www.w3school.com.cn"&gt;W3School&lt;/a&gt;</pre>

<p class="tiy"><a target="_blank" href="/tiy/t.asp?f=html_a">亲自试一试</a></p>
</div>

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
