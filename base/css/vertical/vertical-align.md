#web前端如何实现CSS竖向居中

<h2>
  使用Flexbox实现CSS竖向居中
</h2>
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

<div style="display: inline-block;margin-right: 20px;padding-bottom: 30px;margin-left: 2em;">
    <a style="color: #ffffff;text-decoration: none;font-weight: normal;
    background-color: #24890d;
    border: 0;
    padding: 10px 30px 11px;
    text-transform: uppercase;
    vertical-align: bottom;
    border-radius: 2px;"  href="http://sevenhao.github.io/case/case-about-css/Flexbox-vertical.html">示例演示</a>
  </div>
  
  
  <h2>理解vertical-align或“如何竖向居中”</h2>
  <div>
    <p>vertical-align 不同使用场合的理解/p>
  </div>
  <h3>1、Table单元格中的vertical-align</h3>
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
  
  
  <h3>2、vertical-align在inline元素上效果</h3>
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
  
  
   <h3>3、vertical-align在其它元素上的效果</h3>
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
    <a href="http://sevenhao.github.io/case/case-about-css/block-vertical-eg1.html">示例演示</a>
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
    <a href="http://sevenhao.github.io/case/case-about-css/block-vertical-eg2.html">示例演示</a>
  </div>


<h2>三、竖向居中最简单的方法(三行CSS3代码)</h2>
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
    <a href="http://sevenhao.github.io/case/case-about-css/justify-content-vertical.html">示例演示</a>
</div>
