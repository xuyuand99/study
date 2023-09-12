# HTML

## 1.列表

##### 1.有序列表

##### <h2&gt;要把大象放冰箱总共分几步</h2>
<ol&gt;
<li&gt;把冰箱门打开</li&gt;
<li\>把大象放进去</li&gt;
<li\>把冰箱门关上</li&gt;
</ol\>

##### 2.无序列表

<h2&gt;我想去的几个城市</h2>

<ul&gt;
<li>成都</li>
<li>上海</li>
<li>西安</li>
<li>武汉</li>
</ul>

##### 3.自定义列表

所谓自定义列表，就是一个包含术语名称以及术语描述的列表。

一个 dl 就是一个自定义列表，一个 dt 就是一个术语名称，一个 dd 就是术语描述

<dl&gt;
    <dt>xxxxxxx</dt>
    <dd>xxxxxxxxxxxxx</dd>
</dl>

## 2.表格

![](C:\Users\黄旭\Desktop\screenshot20230912.png)

![](C:\Users\黄旭\Downloads\screenshot20230913.png)

tr ：每一行 

th 、 td ：每一个单元格（备注：表格头部中用 th ，表格主体、表格脚注中用： td ）

###### table:含义为表格 

属性：width ：设置表格宽度。 height ：设置表格最小高度，表格最终高度可能比设置 的值大。 border ：设置表格边框宽度。 cellspacing ： 设置单元格之间的间距。

###### thead:含义为表格头部

height ：设置表格头部高度。
align ： 设置单元格的水平对齐方式，可选值如下：
1. left ：左对齐
2. center ：中间对齐
3. right ：右对齐

valign ：设置单元格的垂直对齐方式，可选值如下：

​	 top ：顶部对齐

 	middle ：中间对齐

 	bottom ：底部对齐

###### tbody:表格主体

属性同thead

###### tfoot:表格脚注

同上

###### tr:行

同上

###### td:普通单元格

width ：设置单元格的宽度，同列所有单元格全都受影 响

 heigth ：设置单元格的高度，同行所有单元格全都受影 响。

 align ：设置单元格的水平对齐方式。 

valign ：设置单元格的垂直对齐方式。

 rowspan ：指定要跨的行数。 

colspan ：指定要跨的列数。

###### th:表头单元格

同上

#### 注：

1. 元素的 border 属性可以控制表格边框，但 border 值的大小，并不控制单元格 边框的宽度， 只能控制表格最外侧边框的宽度，这个问题如何解决？—— 后期靠 CSS 控制。
2. 默认情况下，每列的宽度，得看这一列单元格最长的那个文字。 
3. 给某个 th 或 td 设置了宽度之后，他们所在的那一列的宽度就确定了 
4. 给某个 th 或 td 设置了高度之后，他们所在的那一行的高度就确定了。
5. rowspan ：指定要跨的行数。 colspan ：指定要跨的列数。

## 3.常用标签 \>

<br &gt;换行

<hr&gt;分割

<pre&gt;按照原文的输入来显示

## 4.表单

### 1.基本结构

###### 1.form（表单）

action ：用于指定表单的提交地址（需要与后端人员沟通后确
定）。
target ：用于控制表单提交后，如何打开页面，常用值如下：
_self ：在本窗口打开。
_blank ：在新窗口打开。

###### 2.input（输入框）

type ：设置输入框的类型

name ：用于指定提交数据的名字

###### 3.button(按钮)

实例：

&lt; form action="https://www.baidu.com/s" target="_blank" method="get">
&lt; input type="text" name="wd">
< button>去百度搜索</button>
< /form>

### 2.常用控件

##### 1.文本输入

<input type="text">

属性：

name 属性：数据的名称。

 value 属性：输入框的默认输入值。 

maxlength 属性：输入框最大可输入长度。

##### 2.密码输入

<input type="password">

属性：

name 属性：数据的名称。
value 属性：输入框的默认输入值（一般不用，无意义）。
maxlength 属性：输入框最大可输入长度。

##### 3.单选框

<input type="radio" name="sex" value="female">女
<input type="radio" name="sex" value="male">男

属性：

name 属性：数据的名称，注意：想要单选效果，多个 radio 的 name 属性值要保持一致。
value 属性：提交的数据值。
checked 属性：让该单选按钮默认选中。

##### 4.多选框

<input type="checkbox" name="hobby" value="smoke">抽烟
<input type="checkbox" name="hobby" value="drink">喝酒
<input type="checkbox" name="hobby" value="perm">烫头

属性：

name 属性：数据的名称。

 value 属性：提交的数据值。 

checked 属性：让该复选框默认选中。

##### 5.隐藏域

<input type="hidden" name="tag" value="100">

用户不可见的一个输入区域，作用是： 提交表单的时候，携带一些固定的数据。

 name 属性：指定数据的名称。 value 属性：指定的是真正提交的数据。

##### 6.按钮

<input type="submit" value="点我提交表单">
<button>点我提交表单</button>



<input type="reset" value="点我重置">
<button type="reset">点我重置</button>



<input type="button" value="普通按钮">
<button type="button">普通按钮</button>

##### 9.文本域

textarea name="msg" rows="22" cols="3">我是文本域</textarea>

##### 10.下拉框

<select name="place">
            <option value="冀">河北</option>
            <option value="鲁" selected>山东</option>
           < option value="粤">广东</option>
</select>

1. name 属性：指定数据的名称。
2. option 标签设置 value 属性， 如果没有 value 属性，提交的数据是 option 中间的文
字；如果设置了 value 属性，提交的数据就是 value 的值（建议设置 value 属性）
3. option 标签设置了 selected 属性，表示默认选中。

##### 11.disabled 禁用

##### 12.label关联

##### 13.fieldset 与 legend

## 5.框架标签iframe

name ：框架名字，可以与 target 属 性配合。 width ： 框架的宽。 height ： 框架的高度。 frameborder ：是否显示边框，值：0 或者1。

## 6.html实体

 空格 & nbsp;

小于号&amp; lt;

大于号&  gt; 

## 7.全局标量

## 8.mate元信息