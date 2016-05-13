# meta标签

<div>
<h2>定义和用法</h2>

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

## 声明文档使用的字符编码
```
<meta charset='utf-8'>
```

## 用IE浏览页面时，让浏览器用本机上最新的IE渲染引擎
```
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

## 页面描述
每个网页都应有一个不超过 150 个字符且能准确反映网页内容的描述标签。
```
<meta name="description" content="描述内容" />
```

## 页面关键词
```
<meta name="keywords" content="关键词1,关键词2"/>
```

## 定义网页搜索引擎索引方式
```
<meta name="robots" content="index,follow" />
```
详细描述见[这里](http://msdn.microsoft.com/zh-cn/library/ff724037%28v=expression.40%29.aspx)

## 网页作者
```
<meta name="author" content="作者名"/>
```

## viewport(移动设备)
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

## 拓展阅读
* [所有meta标签列表](http://code.lancepollard.com/complete-list-of-html-meta-tags/)
* [常用的 HTML 头部标签](https://github.com/yisibl/blog/issues/1)
