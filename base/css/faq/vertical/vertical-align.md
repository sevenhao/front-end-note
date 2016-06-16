#web前端如何实现CSS竖向居中

## 目录
* [使用Flexbox实现CSS竖向居中](#vercital1)
* [理解vertical-align或“如何竖向居中”](#vercital2)
  * [Table单元格中的vertical-align](#va1)
  * [vertical-align在inline元素上效果](#va2)
  * [vertical-align在其它元素上的效果](#va3)
* [竖向居中最简单的方法(三行CSS3代码)](#vercital3)
* [常见简单垂直剧中方法比较](#vercital4)


## <a name="vercital1">一、使用Flexbox实现CSS竖向居中</a>
  
<div>
  <p>竖向居中需要一个父元素和一个子元素合作完成</p>
</div>

```
<div class="flexbox-container">
  <div class="flexbox-vert-item">Blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah </div>
  <div class="flexbox-vert-item">Blah blah blah blah blah blah blah blah blah </div>
  <div class="flexbox-vert-item">Blah blah</div>
</div>
```

 <p>但为了让子元素竖向居中，你只需要对父元素施加CSS样式：</p>
```css
.flexbox-container {
  padding: 20px;
  background: #eee;

  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;

  -ms-flex-align: center;
  -webkit-align-items: center;
  -webkit-box-align: center;

  align-items: center;
}

.flexbox-vert-item {
  width: 300px;
  background: #fefefe;
  margin-right: 20px;
  padding: 10px;
}
```

<p>
因为上面使用了浏览器引擎前缀，所以看起来有些复杂，但实际上本质是非常简单的，也就3句代码。
</p>
```
display: flex;
flex-align: center;
align-items: center;
```

<div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/Flexbox-vertical.html">示例演示</a>
</div>


## <a name="vercital2">二、理解vertical-align或如何竖向居中</a> 

  <div>
    <p>vertical-align 不同使用场合的理解/p>
  </div>
 
  
### <a name="va1">1、Table单元格中的vertical-align</a>

  <p>
    当出现在Table单元格中时，vertical-align的效果会如大多数人的预期一样，它会跟(老的，不鼓励使用)的valign属性的作用一样。在现代浏览器里，下面的这三种写法的效果是一样的：
  </p>
  
  ```
  <td valign="middle"> <!-- 这是一种会逐渐被淘汰的用法 --> </td>
  <td style="vertical-align:middle"> ... </td>
  <div style="display:table-cell; vertical-align:middle"> ... </div>
  ```
  <p>在浏览器中，它们的现实效果是下面这样：</p>
  ![image](https://github.com/sevenhao/front-end-note/blob/master/base/css/vertical/vertical.png)
  
  
### <a name="va2">2、vertical-align在inline元素上效果</a>  


  <p>当vertical-align被应用的到inline元素上时，它的作用却是类似(老的，不鼓励使用)的valign属性对<img>的作用一样。在现代浏览器里，下面的这三种写法的效果是一样的：</p>
  
  ```
    <div style="border: 1px solid #e0e0e0">
      <img valign="middle" src="tab_home.png">
      <img style="vertical-align:middle"  src="tab_home_pre.png">
      <span style="display:inline-block; vertical-align:middle"> 示例 </span>
    </div>
  ```
  
  ```
    <div style="border: 1px solid #e0e0e0;margin-top: 10px;">
      <img valign="middle" src="tab_home.png">
      <img style="vertical-align:middle"  src="tab_home_pre.png">
      <span style="display:inline-block; vertical-align:bottom"> 示例 </span>
    </div>
  ```
  <p>用<code><span style="display:inline-block; vertical-align:middle"> 示例 </span></code>和<code><span style="display:inline-block; vertical-align:bottom"> 示例 </span></code>作为例子，在浏览器中，它们的现实效果是下面这样：</p>
  ![image](https://github.com/sevenhao/front-end-note/blob/master/base/css/vertical/inline-vertical-align.png)
  
  <p>由此可见，valign="middle"和vertical-align:bottom用在inline元素上的效果是一样。</p>
  
  
### <a name="va3">3、vertical-align在其它元素上的效果</a>   

 
  <p>
    将vertical-align属性应用到一个block元素(例如标准的<div>)上时，大多数浏览器会依照继承的原则，将所有它的inline子元素也应用这个属性。那么，如何将一个元素竖向居中？
  </p>
  
  <h4>方法一</h4>
  
#####前提
  * 你需要把想要竖向居中的内容放到一个block元素中，并给这个想要居中的元素指定固定的高度。
  * 绝对定位(absolutely-position)这个元素。(通常这样做是没问题的，因为你这个想要居中的元素的父元素仍然可以使用相对位置)。
  
  
#####方法
  * 指定父元素为position:relative 或 position:absolute。
  * 给子元素指定固定的高度。
  * 给子元素设定position:absolute 以及 top:50%，让子元素移动到父元素内部上下居中的位置。
  * 给子元素设定 margin-top:-yy，这里的 yy 的值是你的子元素的高度的一半，弥补居中时的偏差。

  ```CSS代码
  <style type="text/css">
    #myoutercontainer {
      position: relative;
      height: 13em;
      border: 1px solid black;
    }
    #myinnercontainer {
      position: absolute;
      top: 50%;
      height: 6em;
      margin-top: -3em;
    }
  </style>
  ```
  
  
   ```HTML代码
  <div id="myoutercontainer">
    <div id="myinnercontainer">
      <p>Hi,我竖向居中了！</p>
      <p>感觉很犀利的哦!</p>
    </div>
  </div>
  ```
  <div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/block-vertical-eg1.html">示例演示</a>
  </div>
  
  
<h4>方法二</h4>
#####前提
* 需要竖向居中的内容只有一行文字。
* 需要对父元素设定固定的高度。


#####方法
* 将父元素的line-height设置为你想要的高度。


  ```CSS代码
  <style type="text/css">
    #myoutercontainer2 {
      line-height: 4em;
      border: 1px solid black;
    }
  </style>
  ```

  
   ```HTML代码
  <div id="myoutercontainer2">嗨，我竖向居中了，耶！</div>
  ```
  <div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/block-vertical-eg2.html">示例演示</a>
  </div>

## <a name="vercital3">三、竖向居中最简单的方法(三行CSS3代码)</a>
<div>
  <p>只用三行CSS3代码，就会完美的让任何元素竖向居中</p>
</div>

 ```CSS代码
.parent-element {
    display: flex;
    justify-content: center;
    align-items: center;
    background: #a3c8fc;
  }
 ```
 
  ```HTML代码
<div class="parent-element">
  <p class="element ">hello world!
  </p>
</div>
 ```
 
 <p>如果想兼容老式的浏览器，你需要在transform属性前添加浏览器引擎前缀。</p>
```CSS代码
.parent-element {
    display: flex;
    justify-content: center;
    -webkit-justify-content: center;
    -ms-justify-content: center;
    -moz-justify-content: center;
    align-items: center;
    background: #a3c8fc;
  }
 ```
 
 <div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/justify-content-vertical.html">示例演示</a>
</div>


## <a name="vercital4">常见简单垂直剧中方法比较</a>

### 方法一

<p>这个方法把一些 div 的显示方式设置为表格，因此我们可以使用表格的 vertical-align property 属性。</p>
```HTML代码
<div id="wrapper">
  <p id="cell">Content goes here</p>
</div>
```

```CSS代码
#wrapper {display:table;height: 50px;background: #e0e0e0;}
#cell {display:table-cell; vertical-align:middle;}
```

优点：
content 可以动态改变高度(不需在 CSS 中定义)。当 wrapper 里没有足够空间时， content 不会被截断

缺点：
Internet Explorer(甚至 IE8 beta)中无效，许多嵌套标签(其实没那么糟糕，另一个专题)

### 方法二

<p>
使用绝对定位的 div，把它的 top 设置为 50％，top margin 设置为负的 content 高度。这意味着对象必须在 CSS 中指定固定的高度。</p>
<p>因为有固定高度，或许你想给 content 指定 overflow:auto，这样如果 content 太多的话，就会出现滚动条，以免content 溢出。</p>

```HTML代码
<div id="content">Content goes here</div>
```

```CSS代码
#content {
   position:absolute;
   top:50%;
   height:240px;
   margin-top:-120px; /* negative half of the height */
   background: #e0e0e0;
 }
```

优点：
适用于所有浏览器
不需要嵌套标签

缺点：
没有足够空间时，content 会消失(类似div 在 body 内，当用户缩小浏览器窗口，滚动条不出现的情况)

<div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/vertical1.html">示例演示</a>
</div>


### 方法三

<p>这种方法，在 content 元素外插入一个 div。设置此 div height:50%; margin-bottom:-contentheight;。</p>
<p>content 清除浮动，并显示在中间。</p>

```HTML代码
<div id="wrapper">
  <div id="floater"></div>
  <div id="content">Content goes here</div>
</div>
```

```CSS代码
#wrapper {height: 400px;background: #a3c8fc}
#floater	{float:left; height:50%; margin-bottom:-120px;}
#content	{clear:both; height:240px; position:relative;background: #e0e0e0;}
```

优点：
适用于所有浏览器
没有足够空间时(例如：窗口缩小) content 不会被截断，滚动条出现

缺点：
唯一我能想到的就是需要额外的空元素了

<div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/vertical3.html">示例演示</a>
</div>


### 方法四

<p>使用了一个 position:absolute，有固定宽度和高度的 div。这个 div 被设置为 top:0; bottom:0;。但是因为它有固定高度，其实并不能和上下都间距为 0，因此 margin:auto; 会使它居中。使用 margin:auto;使块级元素垂直居中是很简单的。</p>

```HTML代码
<div id="wrapper">
  <div id="floater"></div>
  <div id="content">Content goes here</div>
</div>
```

```CSS代码
#wrapper {height: 400px;background: #a3c8fc}
#floater	{float:left; height:50%; margin-bottom:-120px;}
#content	{clear:both; height:240px; position:relative;background: #e0e0e0;}
```

优点：
简单

缺点：
IE(IE8 beta)中无效
无足够空间时，content 被截断，但是不会有滚动条出现

<div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/vertical4.html">示例演示</a>
</div>

### 方法五

<p>只能用于单行文本置中。只需要简单地把 line-height 设置为那个对象的 height 值就可以使文本居中了。</p>

```HTML代码
<div id="content">
  单行文本置中
</div>
```

```CSS代码
#content {height:100px; line-height:100px;  border: 1px solid #000000;}
```

优点：
适用于所有浏览器
无足够空间时不会被截断

缺点：
只对文本有效(块级元素无效)
多行时，断词比较糟糕

<div >
    <a href="http://sevenhao.github.io/case/case-about-css/vertical/vertical5.html">示例演示</a>
</div>
