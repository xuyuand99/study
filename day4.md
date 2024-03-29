# css

## 选择器优先级(详细)

### 1.计算方式：

每个选择器，都可计算出一组权重，格式为： (a,b,c)

 a : ID 选择器的个数。

 b : 类、伪类、属性 选择器的个数。

 c : 元素、伪元素 选择器的个数。

例如：

div ul>li p a span     权重：(0,0,6)

\#atguigu .slogan     权重：(1,1,0）

### 2.比较规则：

按照从左到右的顺序，依次比较大小，当前位胜出后，后面的不再对比

例如：

(1,0,0) > (0,2,2)

### 3.特殊

1. 行内样式权重大于所有选择器。
2.  !important 的权重，大于行内样式，大于所有选择器，权重最高！

## 1.css三大特性

层叠性：如果发生了样式冲突，那就会根据一定的规则（选择器优先级），进行样式的层叠（覆 盖）。

继承性：元素会自动拥有其父元素、或其祖先元素上所设置的某些样式。（优先继承离得近的。）

优先级：!important > 行内样式 > ID选择器 > 类选择器 > 元素选择器 > * > 继承的样式

​		详情见上文。

​		计算权重时需要注意：并集选择器的每一个部分是分开算的！

## 2.css常用属性

#### 1.像素  

#### 2.颜色

1. 表示方式一：颜色名

2. 表示方式二：rgb 或 rgba

   编写方式：使用 红、黄、蓝 这三种光的三原色进行组合。
   r 表示 红色
   g 表示 绿色
   b 表示 蓝色
   a 表示 透明度

   注：

   若三种颜色值相同，呈现的是灰色，值越大，灰色越浅。 

    rgb(0, 0, 0) 是黑色， rgb(255, 255,255) 是白色。 

    对于 rbga 来说，前三位的 rgb 形式要保持一致，要么都是 0~255 的数字，要么都是 百分比 。

3. 表示方式三：HEX 或 HEXA

   格式为：# rrggbb

   每一位数字的取值范围是： 0 ~ f ，即：（ 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f ） 所以每一种光的最小值是： 00 ，最大值是： ff

4. 表示方式四：HSL 或 HSLA

   HSL 是通过：色相、饱和度、亮度，来表示一个颜色的，格式为： hsl(色相,饱和度,亮度)

   色相：取值范围是 0~360 度

   饱和度：取值范围是 0%~100% 。（向色相中对应颜色中添加灰色， 0% 全灰， 100% 没有 灰）

   亮度：取值范围是 0%~100% 。（ 0% 亮度没了，所以就是黑色。 100% 亮度太强，所以就是 白色了）

​	HSLA 其实就是在 HSL 的基础上，添加了透明度。

#### 3.文本属性

1.文本颜色

属性名： color 

作用：控制文字的颜色。 

可选值： 1. 颜色名 2. rgb 或 rgba 3. HEX 或 HEXA （十六进制） 4. HSL 或 HSLA

2 文本间距 

字母间距： letter-spacing 

单词间距： word-spacing （通过空格识别词） 

属性值为像素（ px ），正值让间距增大，负值让间距缩小。

3 文本修饰 

属性名： text-decoration 

作用：控制文本的各种装饰线。 

可选值： 1. none ： 无装饰线（常用） 2. underline ：下划线（常用） 3. overline ： 上划线 4. line-through ： 删除线 

可搭配如下值使用： 1. dotted ：虚线 2. wavy ：波浪线 3. 也可以指定颜色