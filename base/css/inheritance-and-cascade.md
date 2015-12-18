## 样式的继承
CSS样式表继承指的是，特定的CSS属性向下传递到子孙元素。    
需要注意的是
> * 只有某些样式规则会继承
> * 样式规则是否继承是由浏览器决定的

### 会继承的样式规则
会继承的样式主要包括：
>  * 字体相关的：
       * font-family(字体系列), 
       * font-size(继承计算后的值), 
       * font-style(斜体、倾斜或正常字体),
       * font-variant(小型大写字母), 
       * font-weight(normal,bold,bolder,lighter), 
       * font(font:italic bold 12px/20px arial,sans-serif;) ,
       * letter-spacing(字符间距),
       * line-height（行间的距离）
<br>
> * 文本：
       * text-indent(首行缩进), 
       * text-align(水平对齐方式), 
       * layout-flow, 
       * writing-mode(lr-tb：从左向右，从上往下;tb-rl：从上往下，从右向左), 
       * white-space(如何处理元素内的空白), 
       * word-wrap(允许长单词换行到下一行), 
       * text-kashida-space, 
       * layout-grid, 
       * layout-grid-char, 
       * layout-grid-char-spacing, 
       * layout-grid-line, 
       * layout-grid-mode, 
       * layout-grid-type
<br>
> * 列表相关的：
       * list-style-image(属性使用图像来替换列表项的标记，[实例](http://www.w3school.com.cn/cssref/pr_list-style-image.asp)), 
       * list-style-position（何处放置列表项标记）,
       * list-style-type（列表项标记的类型,[实例](http://www.w3school.com.cn/tiy/t.asp?f=csse_list-style-type_test)）, 
       * list-style(一个声明中设置所有的列表属性,按顺序设置如下属性：list-style-type、list-style-position、list-style-image)
<br>
> * 表格：
       * border-collapse(表格的边框是否被合并为一个单一的边框,[实例](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border-collapse)), 
       * border-spacing(相邻单元格的边框间的距离,[实例](http://www.w3school.com.cn/tiy/t.asp?f=csse_table_border-spacing)), 
       * caption-side(设置表格标题的位置), 
       * empty-cells(是否显示表格中的空单元格), 
       * table-layout, 
       * speak-header

### 选择器权重
各类选择器的权重得分
> * 带 !important 的规则得分是最高的
> * 行内样式（style="..."）1000分
> * ID选择器 100分
> * 类选择器，伪类选择器，属性选择器 10分
> * 标签选择器，伪元素选择器 1分
> * 通配选择器 0分
> * 继承和浏览器默认的的样式的得分是最低的

因此，越特定的选择器，权重越高。

当有多个规则都能应用于同一个元素时，权重越高的样式将被优先采用。若权重相同，则后定义的被采用。
任何一条与css继承值冲突的属性值都会覆盖继承的属性值。

详细介绍可见（ http://css-tricks.com/specifics-on-css-specificity/）
