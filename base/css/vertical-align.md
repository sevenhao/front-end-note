#web前端如何实现CSS竖向居中

<h2>
  使用Flexbox实现CSS竖向居中
</h2>
<div>
  <p>竖向居中需要一个父元素和一个子元素合作完成</p>
</div>

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

```
<div class="flexbox-container">
  <div class="flexbox-vert-item">Blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah </div>
  <div class="flexbox-vert-item">Blah blah blah blah blah blah blah blah blah </div>
  <div class="flexbox-vert-item">Blah blah</div>
</div>
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
