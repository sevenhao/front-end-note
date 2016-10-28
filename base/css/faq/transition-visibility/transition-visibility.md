#transition与visibility 延时隐藏

## 目录
* [transition与visibility介绍](#vercital1)
* [transition实现元素的自动延时隐藏](#vercital2)
* [transition-delay做延时](#vercital3)
* [元素淡出动画结束后自动隐藏](#vercital4)


## <a name="vercital1">一、transition与visibility介绍</a>
  
<div>
  <p>visibility: 离散步骤，在0到1数字范围之内，0表示“隐藏”，1表示完全“显示”</p>
  <p>visibility:hidden可以看成visibility:0；</p>
  <p>visibility:visible可以看成visibility:1.</p>
  <p>于是，visibility应用transition等同于0~1之间的过渡效果。</p>
  <p>只要visibility的值大于0就是显示的。我们可以利用transition实现元素的自动<strong>延时隐藏</strong>。</p>
  <p><strong>注意：</strong>只支持IE10+以及其他现代浏览器。</p>
</div>



## <a name="vercital2">二、transition实现元素的自动延时隐藏</a> 

  <div>
    <p>我们实现非嵌套多级菜单以及其他一些需要延时隐藏交互效果提供了新的灵感——CSS控制，而非JS中的setTimeout定时器</p>
  </div>
  
   ```
  <div class="hover">
    <img src="http://ww2.sinaimg.cn/mw1024/8df570cejw1e3dwpgboytj.jpg" class="trans image" />
    <a href="#">鼠标划过显示图片</a>
  </div>
  ```
  
   ```
   .trans{
      -webkit-transition:all 0.5s ease;
      -moz-transition:all 0.5s ease;
      -o-transition:all 0.5s ease;
      -ms-transition:all 0.5s ease;
      transition:all 0.5s ease;
   }
   .image{position:absolute; margin-top:20px; visibility:hidden;}
   .hover:hover .image{visibility:visible;}
   ```
   
   [点击查看延时隐藏demo](https://codepen.io/qhao/pen/dXXzJb)
  

## <a name="vercital3">三、transition-delay做延时</a>
<div>
  <p>transition中有个属性叫做transition-delay就是做延时</p>
</div>

 ```CSS代码
.trans-delay{
    -webkit-transition:visibility 0s linear;
    -moz-transition:visibility 0s linear;
    -o-transition:visibility 0s linear;
    -ms-transition:visibility 0s linear;
    transition:visibility 0s linear;
}
.image-delay{position:absolute; margin-top:20px; visibility:hidden;
    -webkit-transition-delay:0s;
    -moz-transition-delay:0s;
    -ms-transition-delay:0s;
    -o-transition-delay:0s;
    transition-delay:0s;
}
.hover-delay:hover .image-delay{
    visibility:visible;
    -webkit-transition-delay:0.5s;
    -moz-transition-delay:0.5s;
    -ms-transition-delay:0.5s;
    -o-transition-delay:0.5s;
    transition-delay:0.5s;
}
 ```
 
  ```HTML代码
<div class="hover-delay">
    <img src="http://ww2.sinaimg.cn/mw1024/8df570cejw1e3dwpgboytj.jpg" class="trans-delay image-delay" />
    <a href="#">鼠标划过显示图片</a>
</div>

 ```
 
[点击查看延时隐藏demo](https://codepen.io/qhao/pen/KMMvQZ)


## <a name="vercital4">元素淡出动画结束后自动隐藏</a>


<p>我们要实现淡入淡出效果，显然是需要改变透明度的，但是，元素即使透明度变成0，虽然肉眼看不见，但是，在页面上，元素还是可以点击，还是可以覆盖其他元素的，这显然是有问题的，我们最最希望的是在元素淡出动画结束后，元素可以自动隐藏！visibility的响应就是为这个需求而生的！</p>
<p>图片透明度慢慢降低成0后，图片就立即自动应用了visibility:hidden, 实现了配合天衣无缝的隐藏。</p>
<p>display:none无法应用transition效果，甚至是破坏作用。</p>


```HTML代码
<div class="hover-fadeout">
    <img src="http://ww2.sinaimg.cn/mw1024/8df570cejw1e3dwpgboytj.jpg" class="trans-fadeout image-fadeout" />
    <a href="#">鼠标划过显示图片</a>
</div>
```

```CSS代码
.trans-fadeout{
   -webkit-transition:all 0.5s linear;
   -moz-transition:all 0.5s linear;
   -ms-transition:all 0.5s linear;
   -o-transition:all 0.5s linear;
   transition:all 0.5s linear;
}
.image-fadeout{position:absolute; margin-top:20px; visibility:hidden; opacity:0;}
.hover-fadeout:hover .image-fadeout{ visibility:visible; opacity:1; }
```

[点击查看延时隐藏demo](https://codepen.io/qhao/pen/EyyvEr)


非常感谢张鑫旭大神分享，本文是对于他分享方法的自我验证与记录。
原谅地址：http://www.zhangxinxu.com/wordpress/2013/05/transition-visibility-show-hide/
