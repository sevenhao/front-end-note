## 大话浮动

浮动(float)，是一个好用但用好不易的属性。通过浮动，我们能很方便地布局，但是浮动之后遗留下来太多的问题需要解决，特别是IE6-7。


### 一、清除浮动 还是 闭合浮动 
**1）清除浮动**：清除对应的单词是clear，对应CSS中的属性是 clear：left | right | both | none；

清除浮动示例代码如下：

html代码

```
<div class="content1">
    <h4>清除浮动</h4>
    <div class="wrap">
      <div class="main left">左一float:left，问题：现代浏览器中无法把wrap撑高</div>
      <div class="side left">左二float:left</div>
    </div>

    <div class="footer clear">div2 clear:both <strong>清除浮动</strong>,
      <br>虽然位置正确了,但是 wrap 的高度没变
    </div>
    <div class="explain">
      <span class="result">结果:</span>
      通过在footer上设置clear：both，清除浮动，footer位置正确，但是并不能解决wrap高度塌陷的问题。
    </div>
  </div>
```

---

CSS代码：

```
h2{
      font-size: 24px;
      margin: 20px 0;
      text-align: center;
      color: #555;
    }
    h3{
      font-size: 18px;
      margin: 20px 0;
      color: #555;
    }
    div {
      padding: 15px 20px;
      font-size: 14px;
      color: #333;
    }
    .left {
      float: left;
    }
    .clear {
      clear: both;
    }
    .wrap {
      border: 1px solid red;
      width: 600px;
      margin: 30px auto 5px;
      background: #f0f0f0;
    }
    .main {
      height: 60px;
      width: 50%;
      background: #38BA9B;
      color: #ffffff;
      font-size: 16px;
    }
    .side {
      width: 20%;
      background: #F8B726;
      color: #ffffff;
      font-size: 16px;
    }
    .footer {
      border: 1px solid #CCC;
      background: #EEE;
      width: 600px;
      margin: 5px auto 30px;
      font-size: 16px;
    }
    .explain{
      width: 600px;
      margin: 5px auto 30px;
      font-size: 16px;
      background: #ffecec;
    }
    .result{
      font-size: 18px;
      font-weight: bold;
      color: red;
    }
```


---


**2）闭合浮动**：更确切的含义是使浮动元素闭合，从而减少浮动带来的影响。

闭合浮动示例代码如下：

html代码

```
<div class="content1">
    <h4>闭合浮动</h4>
    <div class="wrap clearfix">
      <div class="main left">左一float:left后，自己闭合浮动了，所以footer不用再清除浮动了</div>
      <div class="side left">左二float:left</div>
    </div>

    <div class="footer clear">div2：这次 通过在wrap添加 .clearfix ，通过.clearfix:after已经
      <strong>闭合浮动</strong>
    </div>
    <div class="explain">
      <span class="result">结果:</span>
      通过在wrap添加 .clearfix ，通过.clearfix:after已经闭合浮动，不再出现wrap高度塌陷的问题。
    </div>
  </div>
```

---
CSS代码，在清除浮动css基础上添加以下代码

```
.clearfix:after {
      clear: both;
      content: ".";
      display: block;
      height: 0;
      visibility: hidden;
    }
```

请查看[==示例demo验证==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#distinguish)，通过实例可发现，其实我们想要达到预想的效果，在应用float后，应该做的是闭合浮动，而不是单纯的清除浮动，在footer上设置clear：both清除浮动并不能解决wrap高度塌陷的问题。  
**结论**：用闭合浮动比清除浮动更加严谨，所以后文中将详细介绍闭合浮动。


### 二、为何要闭合浮动
要解答这个问题，我们得先说说CSS中的定位机制：普通流，浮动，绝对定位 （其中"position:fixed" 是"position:absolute" 的一个子类）。

**1）普通流**：很多人或者文章称之为文档流或者普通文档流，其实标准里根本就没有这个词。如果把文档流直译为英文就是 document flow ，但标准里只有另一个词，叫做 普通流 （normal flow)，或者称之为常规流。

**2）浮动**：浮动框不属于文档中的普通流，它可以左右移动，直至它的外边缘遇到包含框或者另一个浮动框的边缘。

元素浮动之后，不会影响到块级框的布局而只会影响内联框的排列，文档中的普通流就会表现得和浮动框不存在一样，这一点大家可以在清徐浮动示例中去掉footer的clear属性得到验证，footer是块级框，它的排列就跟没有浮动时一样。但是，当浮动框高度超出包含框的时候，也就会出现包含框不会自动伸高来闭合浮动元素（“高度塌陷”现象）。顾名思义，就是漂浮于普通流之上，像浮云一样，但是只能左右浮动。

正是因为浮动的这种特性，导致本属于普通流中的元素浮动之后，包含框内部由于不存在其他普通流元素了，也就表现出高度为0（高度塌陷）。在实际布局中，往往这并不是我们所希望的，所以需要闭合浮动元素，使其包含框表现出正常的高度


浮动对块级元素和内联元素的影响可以看[==示例demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#floatEx)。

### 三、闭合浮动的各种方法
#### 1）添加额外标签
在浮动元素末尾添加一个空的标签例如 <div style=”clear:both”></div>，其他标签br等亦可。

```
<div id="clearFloat1" class="content1">
    <h4>1）添加额外标签</h4>
    <div class="wrap">
      <div class="main left">左一float:left，问题：现代浏览器中无法把wrap撑高</div>
      <div class="side left">左二float:left</div>
      <div style="clear:both;"></div>
    </div>

    <div class="footer">浮动过后的footer块级框</div>
    <div class="explain">
      <span class="result">结果:</span>
      通过添加额外标签清除浮动，布局排列正常
    </div>
  </div>
```

示例详情请查看[==demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#clearFloat1)

**优点**：通俗易懂，容易掌握


**缺点**：可以想象通过此方法，会添加多少无意义的空标签，有违结构与表现的分离。


---

#### 2）使用 br标签和其自身的 html属性
br 自带clear属性标签，可以设置 clear=“all | left | right | none” 属性

```
 <div id="clearFloat2" class="content1">
    <h4>1）使用 br标签和其自身的 html属性</h4>
    <div class="wrap">
      <div class="main left">左一float:left，问题：现代浏览器中无法把wrap撑高</div>
      <div class="side left">左二float:left</div>
      <br clear="all">
    </div>

    <div class="footer">浮动过后的footer块级框</div>
    <div class="explain">
      <span class="result">结果:</span>
      通过添加br元素，并设置clear：all，可以清除浮动，布局排列正常
    </div>
  </div>
```

---
示例详情请查看[==demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#clearFloat2)

**优点**：比空标签方式语义稍强，代码量较少

**缺点**：同样有违结构与表现的分离，不推荐使用


---

#### 3)父元素设置 overflow：hidden

通过设置父元素overflow值设置为hidden；在IE6中还需要触发 hasLayout ，例如 zoom：1；


```
<div id="clearFloat3" class="content1">
    <h4>3）父元素设置 overflow：hidden</h4>
    <div class="wrap" style="overflow:hidden; *zoom:1;">
      <div class="main left">左一float:left，问题：现代浏览器中无法把wrap撑高</div>
      <div class="side left">左二float:left</div>
    </div>

    <div class="footer">浮动过后的footer块级框</div>
    <div class="explain">
      <span class="result">结果:</span>
      通过给父元素添加overflow：hidden属性，可以清除浮动，布局排列正常
    </div>
  </div>
```

---
示例详情请查看[==demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#clearFloat3)

**优点**：不存在结构和语义化问题，代码量少

**缺点**：内容增多时候容易造成不会自动换行导致内容被隐藏掉，无法显示需要溢出的元素。POPO就发现[overflow:hidden会导致中键失效](http://plod.popoever.com/archives/000309.html)。


---

#### 4)父元素设置 overflow：auto 属性

同样IE6需要触发hasLayout，样式结果和3差不多。

示例详情请查看[==demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#clearFloat4)

优点：不存在结构和语义化问题，代码量极少
缺点：多个嵌套后，firefox某些情况会造成内容全选；IE中 mouseover造成宽度改变时会出现最外层模块有滚动条等，firefox早期版本会无故产生focus等。


---

#### 5）父元素也设置浮动
优点：不存在结构和语义化问题，代码量极少
缺点：使得与父元素相邻的元素的布局会受到影响，不可能一直浮动到body，不推荐使用


---
#### 6）父元素设置display:table

示例详情请查看[==demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#clearFloat5)

**优点**：结构语义化完全正确，代码量极少

**缺点**：盒模型属性已经改变，由此造成的一系列问题，得不偿失，不推荐使用


---
#### 7）使用:after 伪元素
需要注意的是 :after是伪元素（Pseudo-Element），不是伪类（某些CSS手册里面称之为“伪对象”），很多闭合浮动大全之类的文章都称之为伪类，不过csser要严谨一点，这是一种态度。

由于IE6-7不支持:after，使用 zoom:1触发 hasLayout。

就是第一节闭合浮动所介绍的方法。
示例详情请查看[==demo==](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#closeF)

**优点**：结构和语义化完全正确,代码量居中

**缺点**：复用方式不当会造成代码量增加


---

根据以上7种方法，我们可以总结闭合浮动的两类方法：

- **1**，通过在浮动元素的末尾添加一个空元素，设置 clear：both属性，after伪元素其实也是通过 content 在元素的后面生成了内容为一个点的块级元素；

- **2**，通过设置父元素 overflow 或者display：table 属性来闭合浮动


---


### 四、闭合浮动的原理
在CSS2.1里面有一个很重要的概念， Block formatting contexts （**块级格式化上下文**），以下简称 BFC。

CSS3里面对这个规范做了改动，称之为：flow root，并且对触发条件进行了进一步说明。

一个BFC是一个HTML盒子并且至少满足下列条件中的任何一个：

- ###### float的值不为none
- ###### position的值不为static或者relative(即positon为==absolute，fixed==)
- ###### display的值为 table-cell, table-caption, inline-block, flex, 或者 inline-flex中的其中一个
- ###### overflow的值不为visible（overflow为==hidden，auto，scroll== ）
- ###### fieldset元素


---
BFC的特性：

- 1)块级格式化上下文会阻止外边距叠加

当两个相邻的块框在同一个块级格式化上下文中时，它们之间垂直方向的外边距会发生叠加。换句话说，如果这两个相邻的块框不属于同一个块级格式化上下文，那么它们的外边距就不会叠加。

- 2)块级格式化上下文不会重叠浮动元素

根据规定，一个块级格式化上下文的边框不能和它里面的元素的外边距重叠。这就意味着浏览器将会给块级格式化上下文创建隐式的外边距来阻止它和浮动元素的外边距叠加。由于这个原因，当给一个挨着浮动的块级格式化上下文添加负的外边距时将会不起作用。 

- 3)块级格式化上下文通常可以包含浮动

---


##### 触发hasLayout的条件：

###### position: absolute 
 
###### float: left|right 
 
###### display: inline-block 
 
###### width: 除 “auto” 外的任意值 
 
###### height: 除 “auto” 外的任意值 （例如很多人闭合浮动会用到 height: 1%  ） 
 
###### zoom: 除 “normal” 外的任意值 
 

在 IE7 中，overflow 也变成了一个 layout 触发器：
###### overflow: hidden|scroll|auto 
（ 这个属性在IE之前版本中没有触发 layout 的功能。 ）
 
###### overflow-x|-y: hidden|scroll|auto 
（CSS3 盒模型中的属性，尚未得到浏览器的广泛支持。他们在之前IE版本中同样没有触发 layout 的功能）



---
综上所述：

**在支持BFC的浏览器（IE8+，firefox，chrome，safari）通过创建新的BFC闭合浮动；**

**在不支持 BFC的浏览器 （IE6-7），通过触发 hasLayout 闭合浮动。**

 

---

### 五、值得选择的闭合浮动方法

通过第三节分析的原理，我们发现其实更多的：display：table-cell，display：inline-block等只要触发了BFC的属性值都可以闭合浮动。从各个方面比较，after伪元素闭合浮动无疑是相对比较好的解决方案了，下面详细说说该方法。
.clearfix:after {content:"."; display:block; height:0; visibility:hidden; clear:both; }
.clearfix { *zoom:1; }
1.  display:block 使生成的元素以块级元素显示,占满剩余空间;

2.  height:0 避免生成内容破坏原有布局的高度。

3.  visibility:hidden 使生成的内容不可见，并允许可能被生成内容盖住的内容可以进行点击和交互;

4.  通过 content:"."生成内容作为最后一个元素，至于content里面是点还是其他都是可以的，例如oocss里面就有经典的 content:"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",有些版本可能content 里面内容为空,一丝冰凉是不推荐这样做的,firefox直到7.0 content:”" 仍然会产生额外的空隙；

5.  zoom：1 触发IE hasLayout。
通过分析发现，除了clear：both用来闭合浮动的，其他代码无非都是为了隐藏掉content生成的内容，这也就是其他版本的闭合浮动为什么会有font-size：0，line-height：0。


---


###### 精益求精方案一：
相对于空标签闭合浮动的方法代码似乎还是有些冗余，通过查询发现Unicode字符里有一个“零宽度空格”，也就是U+200B ，这个字符本身是不可见的，所以我们完全可以省略掉 visibility:hidden了

```
.clearfix:after {
    content:"200B"; 
    display:block; 
    height:0; 
    clear:both; 
}
.clearfix { *zoom:1; }
```
.


###### 精益求精方案二：
由Nicolas Gallagher 大湿提出来的,原文:A new micro clearfix hack，该方法也不存在firefox中空隙的问题。

```
/* For modern browsers */
.cf:before,.cf:after {
    content:"";
    display:table;
}
.cf:after { clear:both; }/* For IE 6/7 (trigger hasLayout) */
.cf { zoom:1; }
```

[示例详情demo](http://sevenhao.github.io/case/case-about-css/float/clearfloat.html#clearFloatGood)

**需要注意的是：**

上面的方法用到了：before伪元素，很多人对这个有些迷惑，到底我什么时候需要用before呢？为什么方案一没有呢？其实它是用来处理margin边距重叠的，由于内部元素 float 创建了BFC，导致内部元素的margin-top和 上一个盒子的margin-bottom 发生叠加。如果这不是你所希望的，那么就可以加上before，如果只是单纯的闭合浮动，after就够了！并不是如同大漠《Clear Float》一文所说的：但只使用clearfix:after时在跨浏览器兼容问题会存在一个垂直边距叠加的bug，这不是bug，是BFC应该有的特性。


本文转自http://www.iyunlu.com/view/css-xhtml/55.html
（怕以后找不到故部分改写并copy到自己的github，非常感谢原文作者）
参考http://www.zhangxinxu.com/wordpress/?p=621
