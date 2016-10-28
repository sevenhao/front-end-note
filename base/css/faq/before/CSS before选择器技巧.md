# CSS before选择器技巧

## 什么是:before和:after？ 该如何使用他们？
- before是css中的一种伪元素，可用于在某个元素之前插入某些内容。
- :after是css中的一种伪元素，可用于在某个元素之后插入某些内容。

下面我们先跑个简单的代码测试下效果：

```
<!DOCTYPE>
<html>
<head>
<title>:before和:after测试</title>
<style>
    p:before{
        content: "H"  /*:before和:after必带技能，重要性为满5颗星*/
    }
    p:after{
        content: "d"  /*:before和:after必带技能，重要性为满5颗星*/
    }
  </style>
</head>

<body>
<p>ello Worl</p>
</body>
</html>
```

以上的代码将会在页面中展现的是"Hello World"。我们通过浏览器的"审查元素"看到的内容是：

```
<p>
  ::before
  "ello Worl"
  ::after
</p>
```
***p***标签内部的内容的前面会被插入一个:before伪元素，该伪元素内包含的内容是"H"；而在p标签内的内容后面会被插入一个:after伪元素，该元素包含的内容是"d"。作为一只合格的程序猴子，捍卫"Hello World"的完整存在是必要的。

##
## 1.结合border写个对话框的样式。
### 用border画三角形样式

```
<!DOCTYPE>
<html>
<head>
<title>triangle</title>
<style>
    .triangle{
        width: 0;
        height: 0;
        border-left:50px solid red;
        border-bottom:50px solid blue;
        border-top:50px solid black;
        border-right:50px solid purple    
		}
  </style>
</head>

<body>
 <div class="triangle"></div>
</body>
</html>
```

以上代码将会在页面上展示一个正方形，左边是个红色的三角形，右边是紫色的三角形，上面是黑色的三角形，下面是蓝色的三角形。如下图所示：

![image](https://github.com/sevenhao/front-end-note/blob/master/base/css/faq/before/triangle.png)


我们对上面的样式做些修改：
```

  .triangle{
      width: 0;
      height: 0;
      border:50px transparent solid; /*这里我们将元素的边框宽度设置为50px，transparent表示边框颜色是透明的，solid表示边框是实线的*/
      border-top-color: black;  /*这里我们仅将上边框的颜色设置为黑色，众所周知，css后面的样式代码会覆盖之前的相同的样式代码，至于其他三边的还是透明色*/
      /*border-bottom-color: black; /*这里设置底部边框色为黑色*/
      border-left-color: black;  /*这里设置左边边框色为黑色*/
      border-right-color:black*/ /*这里设置右边边框色为黑色*/
  }
```

我们就会看到一个在顶部的方向向下的三角形。如下图所示：
![image](https://github.com/sevenhao/front-end-note/tree/master/base/css/faq/before/triangle1.png)

然后我们在样式中加上before:

```
.test-div{
    position: relative;  /*日常相对定位*/
    width:150px;
    height: 36px;
    border:black 1px solid;
    border-radius:5px;
    background: rgba(245,245,245,1);
	margin-left: 100px;		
}
.test-div:before,.test-div:after{
    content: "";  /*:before和:after必带技能，重要性为满5颗星*/
    display: block;
    position: absolute;  /*日常绝对定位*/
    top:8px;
    width: 0;
    height: 0;
    border:6px transparent solid;
}
.test-div:before{
    left:-11px;
    border-right-color: rgba(245,245,245,1);
    z-index:1    
}
.test-div:after{
    left:-12px;
    border-right-color: rgba(0,0,0,1);
    z-index: 0    
}

```

![image](https://github.com/sevenhao/front-end-note/blob/master/base/css/faq/before/triangle2.png)

完整的一个对话框样式就完成了。


##
## 2.作为内容的半透明背景层。

我们的需求是做一个半透明的登录框


```
<!DOCTYPE>
<html>
<head>
<title>triangle</title>
<style>
    body{
        background: url(bg.png) no-repeat left top /*这里加了个图片背景，用以区分背景的半透明及内容的完全不透明*/
    }
    .test-div{
        position: relative;  /*日常相对定位(重要，下面内容也会介绍)*/
        width:300px;
        height: 120px;
        padding: 20px 10px;
        font-weight: bold;
    }
    .test-div:before{
        position: absolute;  /*日常绝对定位(重要，下面内容也会略带介绍)*/
        content: "";  /*:before和:after必带技能，重要性为满5颗星*/
        top:0;
        left: 0;
        width: 100%;  /*和内容一样的宽度*/
        height: 100%;  /*和内容一样的高度*/
        background: rgba(255,255,255,.5); /*给定背景白色，透明度50%*/
        z-index:-1 /*日常元素堆叠顺序(重要，下面内容也会略带介绍)*/
    }
  </style>
</head>

<body>
    <div class="test-div">
        <table>
            <tr>
                <td>Name</td>
                <td><input placeholder="your name" /></td>
            </tr>
            <tr>
                <td>Password</td>
                <td><input placeholder="your password" /></td>
            </tr>
            <tr>
                <td></td>
                <td><input type="button" value="login" /></td>
            </tr>
        </table>
    </div>
</body>
</html>
```

加上张图片可测试效果如下：
![image](https://github.com/sevenhao/front-end-note/blob/master/base/css/faq/before/login.png)
