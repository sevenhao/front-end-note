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
  <h3>Table单元格中的vertical-align</h3>
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
  
  
  <h3>vertical-align在inline元素上效果</h3>
  <p>当vertical-align被应用的到inline元素上时，它的作用却是类似(老的，不鼓励使用)的valign属性对<img>的作用一样。在现代浏览器里，下面的这三种写法的效果是一样的：</p>
  
  ```
  <img align="middle" ...>
  <img style="vertical-align:middle" ...>
  <span style="display:inline-block; vertical-align:middle"> ... </span>
  ```
