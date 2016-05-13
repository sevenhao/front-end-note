# meta标签

## 目录
* [定义和用法](#what)
* [常用标签](#common)


## <a name="what">定义和用法</a>
<div>

<p>&lt;meta&gt; 元素可提供有关页面的元信息（meta-information），比如针对搜索引擎和更新频度的描述和关键词,例如作者、日期和时间、网页描述、关键词、页面刷新等。</p>

<p>&lt;meta&gt; 标签位于文档的头部，不包含任何内容。&lt;meta&gt; 标签的属性定义了与文档相关联的名称/值对。</p>
</div>

<div>
<h2>提示：</h2>

<p><span></span>&lt;meta&gt; 标签永远位于 head 元素内部。</p>

<p><span></span>元数据总是以名称/值的形式被成对传递的。</p>
</div>

<table>
<tbody>
<tr>
<td>
<em>属性</em>
</td>
<td><em>值</em></td>
<td><em>描述</em></td>
</tr>
<tr>
<td>content</td>
<td>字符串</td>
<td>定义与 http-equiv 或 name 属性相关的元信息，属性始终要和 name 属性或 http-equiv 属性一起使用</td>
</tr>
<tr>
<td>http-equiv</td>
<td>content-type、
expires、
refresh、
set-cookie</td>
<td>把 content 属性关联到 HTTP 头部</td>
</tr>
<tr>
<td>name</td>
<td>author、
description、
keywords、
generator、
revised、
others</td>
<td>把 content 属性关联到一个名称。</td>
</tr>
<tr>
<td>scheme</td>
<td>字符串</td>
<td>指定要用来翻译属性值的方案。</td>
</tr>
</tbody>
</table>


## <a name="common">常用标签</a>

### 声明文档使用的字符编码
```
<meta charset='utf-8'>
```

### 用IE浏览页面时，让浏览器用本机上最新的IE渲染引擎
```
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

### 页面描述
每个网页都应有一个不超过 150 个字符且能准确反映网页内容的描述标签。
```
<meta name="description" content="描述内容" />
```

### 页面关键词
```
<meta name="keywords" content="关键词1,关键词2"/>
```

### 定义网页搜索引擎索引方式
```
<meta name="robots" content="index,follow" />
```

<div id="sectionSection0" class="seeAlsoNoToggleSection">
					<p>在 <code>&lt;meta name="robots"&gt;</code> 标记中不正确地使用 
    <strong>nofollow</strong>
   或 
    <strong>noindex</strong>
   属性值可能会显著改变您的网站的搜索引擎结果。</p>
					<p>
						<code>&lt;meta name="robots"&gt;</code> 标记的其他有效属性值包括以下值：</p>
					<ul><li>
							<p>
								
    <strong>follow</strong>
  &nbsp;&nbsp;&nbsp;跟踪链接并分析目标网页。这是默认行为，并且可忽略。</p>
						</li><li>
							<p>
								
    <strong>index</strong>
  &nbsp;&nbsp;&nbsp;将网页编入索引。这是默认行为，并且可忽略。</p>
						</li><li>
							<p>
								
    <strong>noodp</strong>
  &nbsp;&nbsp;&nbsp;不使用 Open Directory Project 来创建内容描述。</p>
						</li><li>
							<p>
								
    <strong>noydir</strong>
  &nbsp;&nbsp;&nbsp;不使用 Yahoo Directory 来创建内容描述。</p>
						</li><li>
							<p>
								
    <strong>noarchive</strong>
  &nbsp;&nbsp;&nbsp;不允许搜索引擎显示内容的缓存版本。</p>
						</li><li>
							<p>
								
    <strong>cache</strong>
  &nbsp;&nbsp;&nbsp;允许搜索引擎显示内容的缓存版本。</p>
						</li><li>
							<p>
								
    <strong>nocache</strong>
  &nbsp;&nbsp;&nbsp;不允许搜索引擎显示内容的缓存版本。</p>
						</li></ul>
				</div>
详细描述见[这里](http://msdn.microsoft.com/zh-cn/library/ff724037%28v=expression.40%29.aspx)

### 网页作者
```
<meta name="author" content="作者名"/>
```

### Refresh （刷新）
说明：让网页多长时间（秒）刷新自己，或在多长时间后让网页自动链接到其它网页。
用法：
```
<Meta http-equiv="Refresh" Content="30">
<Meta http-equiv="Refresh" Content="5; Url=http://www.xia8.net">
```
注意：其中的5是指停留5秒钟后自动刷新到URL网址。


### Copyright (版权)
说明：标注版权转自环 球 网校edu24ol.com转自环 球 网校edu24ol.com转自环 球 网校edu24ol.com
用法：
```
<Meta name="Copyright" Content="本页版权归Zerospace所有。All Rights Reserved">
```


### viewport(移动设备)
```
<meta name ="viewport" content ="initial-scale=1, maximum-scale=3, minimum-scale=1, user-scalable=no"> <!-- `width=device-width` 会导致 iPhone 5 添加到主屏后以 WebApp 全屏模式打开页面时出现黑边 http://bigc.at/ios-webapp-viewport-meta.orz -->
```
content 参数：
* width viewport 宽度(数值/device-width)
* height viewport 高度(数值/device-height)
* initial-scale 初始缩放比例
* maximum-scale 最大缩放比例
* minimum-scale 最小缩放比例
* user-scalable 是否允许用户缩放(yes/no)
* minimal-ui iOS 7.1 beta 2 中新增属性（注意：iOS8 中已经删除），可以在页面加载时最小化上下状态栏。这是一个布尔值，可以直接这样写：`<meta name="viewport" content="width=device-width, initial-scale=1, minimal-ui">`


### iOS 设备
* 添加到主屏后的标题（iOS 6 新增）
```
<meta name="apple-mobile-web-app-title" content="标题"> <!-- 添加到主屏后的标题（iOS 6 新增） -->
```

* 是否启用 WebApp 全屏模式
```
<meta name="apple-mobile-web-app-capable" content="yes"> <!-- 是否启用 WebApp 全屏模式 -->
```


* 设置状态栏的背景颜色
```
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent"> <!-- 设置状态栏的背景颜色，只有在 `"apple-mobile-web-app-capable" content="yes"` 时生效 -->
```
<p>只有在 <code>"apple-mobile-web-app-capable" content="yes"</code> 时生效</p>
<p>content 参数：</p>
<ul>
<li>
<code>default</code> 默认值。</li>
<li>
<code>black</code> 状态栏背景是黑色。</li>
<li>
<code>black-translucent</code> 状态栏背景是黑色半透明。</li>
</ul>
<p>如果设置为 <code>default</code> 或 <code>black</code> ,网页内容从状态栏底部开始。</p>
<p>如果设置为 <code>black-translucent</code> ,网页内容充满整个屏幕，顶部会被状态栏遮挡。</p>


* 禁止数字自动识别为电话号码
```
<meta name="format-detection" content="telephone=no"> <!-- 禁止数字识自动别为电话号码 -->
```

* 禁止自动自动识别地址
```
<meta name="format-detection" content="address=no"> <!-- 禁止自动自动识别地址 -->
```

* 禁止自动自动识别日期
```
<meta name="format-detection" content="date=no">  <!-- 禁止自动自动识别日期 -->
```

* 禁止自动自动识别 Email
```
<meta name="format-detection" content="email=no">  <!-- 禁止自动自动识别 Email -->
```



### 更多介绍
* [meta标签列表](http://code.lancepollard.com/complete-list-of-html-meta-tags/)
* [常用的 HTML 头部标签](https://github.com/yisibl/blog/issues/1)
