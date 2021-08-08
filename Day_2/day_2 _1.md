```
    <head>
        <style>
            /* 要求1, 请将熊大 和 熊而 改为粉色 div &  p*/
            div, p {
                color: pink;
            }


        /* 要求2, 请把胸大和熊二改为红色还有小猪一家改为粉色 */
            div, p, .pg li {
                color: pink;
            }
        /* 约定的语法规范, 我们并集选择器喜欢竖着写 */
    </style>
    </head>
    <body>
        <div> 熊大 </div>
        <p> 熊二 </p>
        <span> 光头强 </span>
        <ul class="pig">
            <li> 小猪 </li>
            <li> 猪爸爸 </li>
            <li> 猪妈妈 </li>
        </ul>
    </body>
```

语法:

```
元素1, 元素2 { 样式声明 }
```

上述语法表示元素1 和 元素2

伪类选择器

伪类选择器用于向某些选择器添加特殊的效果, 比如给链接添加特殊效果, 或选择第1个, 第n个元素
伪类选择器书写最大的特点是用冒号(:) 表示, 比如:hover, :first-child
因为伪类选择器很多, 比如有链接伪类, 结构伪类等, 

```
a:link  /* 选择所有未被访问的链接 */

a:visited /* 选择所有已方位的链接 */

a:hover /* 选择鼠标指针位于其上的链接*/

a:active /* 选择活动链接(鼠标按下未叹气的链接)*/
```

```
    <head>
        <title>符合选择器之伪类选择器</title>
        <style>
            /* 未访问的链接 */
            a:link {
                color: #333;
            }
            a:visited {
                color: orange;
            }
        </style>
    </head>
    <body>
        <a href="#">小猪佩奇</a>
    </body>
```

链接伪类选择器的注意事项
1, 为了确保生效, 请按照LVHA的顺序声明, link - visited - hover - active
2, 因为a链接在浏览器中具有默认样式, 所以我们实际工作中都需要给链接单独指定样式


链接伪类选择器在实际工作开发中的写法

```
    a {
        color: gray;
    }
    a: hover {
        color: red;
    }
```

:focus 伪类选择器用于选取获得焦点的表单元素
焦点就是光标, 一般情况`<input>`类的表单元素才能获取, 因此这个选择器也主要针对于表单元素来说

```
    input:focus {
        brackground-color: yello;
    }
```

```
    <head>
        <style>
            input:focus {
                background-color: pink;
            }
        </style>
    </head>
    <body>
        <input type="text">
        <input type="text">
        <input type="text">
    </body>
```

复合选择器的总结
| 选择器    | 作用    |  特征   |  使用情况   |  隔开符号及用法   |
| --- | --- | --- | --- | --- |
|  后代选择器   |  用来选择后代元素   |  可以是子孙后代   |  较多   |  符号是空格.nov a   |
|  子代选择器   |  选择最近一级元素   |   只选亲儿子  |  较少   |  符号是大于 .nav>p   |
| 并集选择器    |  选择某些相同样式的元素   |  可以用于集体生命   |  较多   |  符号是逗号.nav, .header    |
| 链接伪类选择器    |   选择不同状态的链接  |   跟链接相关  |  较多   |   重点记住 a{} 和 a:hover 实际开发的写法  |
|   :focus选择器  |  选择获得光标的表单   |   跟表单相关  | 较多    |  input:focus 记住这个写法   |


元素显示模式
网页的标签非常多, 在不同地方会用到不同类型的标签, 了解他们的特点,可以更好的布局我们的网页

元素显示模式就是元素(标签)以什么方式进行显示, 比如`<div>`自己占用一行, 比如一行可以放多个`<span>`

html元素一般分为 块元素 和 行内元素两种类型

CSS的元素显示模式
了解元素的显示模式可以更好的让我们布局页面
1, 什么是元素显示模式
2, 元素显示模式的分类
3, 元素显示模式的转换

作用, 网页的标签非常多, 在不同地方会用到不同类型的标签, 了解他们的特点可以更好的布局我们的网页

元素显示模式就是元素(标签)以什么方式进行显示, 比如`<div>`自己占一行, 比如一行可以放多个`<span>`

HTML元素一般分为 块元素 和 行内元素 两种类型

一行可以放好多个就用行内元素, 一行就放一个或特殊情况的就用块元素就可以了


块元素
常见的块元素 有
```
    <h1> ~ <h6>
    <p>
    <div>
    <ul>
    <ol>
    <li>
```

其中`<div>`标签是最典型的块元素

块级元素的标签的特点:
1, 比较霸道, 自己独占一行
2, 高度, 宽度, 外边距 以及内边距都可以控制
3, 宽度默认是容器(父级宽度)的100%
4, 是一个容器及盒子, 里面可以放行内或者块级元素

```
    <body>
        <div> 比较霸道, 自己独占一行 </div>
    </body>
```

注意:
文字类的元素不能使用块级标签
`<p>`标签用于存放文字, 因此`<p>`里面不能放块级元素, 特别是不能放`<div>`
同理, `<h1> ~ <h6>` 等都是文字类块级标签, 里面也不能放其它块级元素

常见的行内元素有`<a>, <strong>, <b>, <em>, <i>, <del>, <s>, <ins>, <u>, <span>`等
其中`<span>`标签是最典型的行内元素, 有的地方也将行内元素称为内联元素

行内元素的特点
1, 相邻内行元素在一行上, 一行可以显示多个
2, 高, 宽直接设置是无效的
3, 默认宽度就是它本身内容的宽度
4, 行内元素只能容纳文本或其它行内元素

注意,
链接里面不能在放链接了,
特殊情况链接 `<a>` 里面可以放块级元素, 但是给`<a>` 转换下一个块级模式最安全

在行内元素中有几个特殊的标签
`<img />， <input />, <td>,` 它们同时具有块元素和行内元素的特点
有些资料成它们为行内块元素

行内块元素的特点:
和相邻行内元素(行内块)在一行上, 但是他们之间会有空白缝隙, 一行可以显示多个(行内元素的特点)
默认宽度就是它本身内容的宽度(行内元素特点)
高度, 行高, 外边距以及内边距都可以控制(块级元素特点)

元素显示模式总结
| 元素模式    | 元素排列    |  设置样式   |  默认宽度   |    包含  |
| --- | --- | --- | --- | --- |
|  块级元素   |  一行只能放一个块级元素    |  可以设置宽度高度    |  容器的100%   |  容器级可以包含任何标签   |
| 行内元素    |  一行可以放多个行内元素   |   不可以直接设置宽度高度  |  它本身内容的宽度   |  容纳文本或则其他行内元素    |
|  行内块元素   |  一行放多个行内块元素   |  可以设置宽度和高度   |  它本身内容的宽度   |     |

特殊情况下, 我们需要元素模式的转换, 简单理解, 一个模式的元素需要另外一种模式的特性
比如想要增加链接 `<a>` 的触发范围

转换为块元素: display: block;
转换为行内元素: display: inline;
转换为行内块: display: inline-block;

```
    <head>
        <style>
        a {
            width :150px;
            height: 50px;
            background-color: pink;
            /* 把行内元素a 转为 块级元素 */
            display: block;
        }
        div {
            width: 300px;
            height: 100px;
            background-color: purple;
            /* 把div块级元素转换为行内元素 */
            display: inlines;
        }
        span {
            width: 100px;
            height: 30px;
            background-color: skyblue;
        }
        </style>
    </head>
    <body>
        <a href="#"> xx </a>
        <a href="#"> oo </a>
        <div> 我是块级元素 </div>
        <div> 我是块级元素 </div>
        <span> 行内元素转换为行内块元素 </span>
        <span> 行内元素转换为行内块元素 </span>
    </body>
```

每一个块级元素可以独占一样, 可以单独设置高度和宽度


```
    <style>
        a {
            display: block;
            width: 230px;
            height: 40px;
            background-color: #55585a;
            font-size: 14px;
            color: #fff;
            text-decoration: none;
            text-indent: 2em;
            line-height: 40px;
            /* 保证height 和 line-height一样就可以了 */
        }
        a: hover {
            background-color: #ff6700;
        }
    <style>
    <body>
        <a href="#"> 手机 电话卡 </a>
        <a href="#"> 电视 盒子 </a>
        <a href="#"> 笔记本 平板 </a>
    </body>
```

2.7 一个小技巧, 单行文字垂直居中的代码
css 没有给我们提供文字垂直居中的代码, 这里我们可以使用一个小技巧来实现
解决方案: 让文字的行高等于盒子的高度, 就可以让文字在当前盒子内垂直居中


2.8 单行文字垂直居中的原理
行高 包括:
1, 上空隙
2, 文字本身的高度
3, 下空隙

盒子高度40
简单理解: 行高的上空隙和下空隙把文字挤到中间了, 是如果行高小于盒子高度, 文字会偏上, 
如果行高大于盒子高度, 则文字偏下

通过CSS背景属性， 可以给页面元素添加背景样式
背景属性可以设置背景颜色, 背景图片, 背景平铺, 背景图片位置， 背景图像固定等

3.1 背景颜色
background-color 属性定义了元素的背景颜色

```
background-color: 颜色值(transparent|color);
```

```
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: transparent;
            /* transparent 透明的,清澈的 */
        }
    </style>
    <body>
        <div></div>
    </body>
```

背景图片
`background-image` 属性描述了元素的背景图像, 实际开发常见于logo或则一些装饰的小图片或是超大的背景图片,
优点是非常便于控制位置(精灵兔也是一种运用场景)

```
background-image: none | url (url)
```

```
    <head>
        <style>
            div {
                width: 300px;
                height: 300px;
                /* 不要落下 url() */
                background-image: url(images/logo.png);
            }
        </style>
    </head>
    <body>
        <div></div>
    </body>
```

背景平铺
如果需要在HTML页面上对北京图像进行平铺,可以使用`background-repeat`属性

```
background-repeat: repeat | no-repeat | repeat-x | repeat-y
```
no-repeat 背景图片不平铺
repeat 默认的情况下, 背景图片是平铺的
repeat-x 沿着x轴平铺
repeat-y 沿着y轴平铺

页面元素既可以添加背景颜色也可以添加背景图片, 只不过背景图片会压住在背景颜色

背景图片位置
利用 `background-position` 属性 可以改变图片在背景图片中的位置

background-position: x, y;

|  参数值   |                       说明                       |
| -------- | ------------------------------------------------ |
| length   | 百分数, 由浮点数字和单位标识符组成的长度值           |
| position | top, center, bottom, left, center, right方位名词 |

1, 参数是方位名词
如果指定的两个值都是方位名词, 则两个值的前后顺序无关，比如 left, top 和 top, left效果一致
如果只指定了一个方位名词, 另一个值省略, 则第二个值默认居中对齐

2, 参数是精确单位
如果参数值是精确坐标, 那么第一个肯定是x坐标, 第二个肯定是y坐标
如果只指定一个数值, 那该数值一定是x坐标, 另一个默认垂直居中

背景图像固定(背景附着)
background-attachment 属性设置背景图像是否固定或者随着页面的其余部分滚动
background-attachment 后期可以制作视差滚动的效果

```
background-attachment: scroll | fixed
```

|  参数   |          作用          |
| ------ | ---------------------- |
| scroll | 背景图像是随对象内容滚动 |
| fixed  | 背景图像固定            |

背景复合写法

为了简化背景属性的代码, 我们可以将这些属性合并简写在同一个属性 background中,从而节约代码量
当使用简写属性时, 没有特定的书写顺序, 一般习惯约定顺序为

```
background: 背景颜色  背景图片地址  背景平铺   背景图像滚动  背景图片位置
```

```
background: transparent   url(image.jpg)   repeat-y   fixed   top;
```
在实际开发中, 我们更提倡的写法

css3为我们提供了背景颜色半透明的效果
```
background: rgba(0，0，0，0.3)
```

|          属性          |      作用      |                      值                       |
| --------------------- | -------------- | --------------------------------------------- |
| background-color      | 背景颜色       | 预定义的颜色值/十六进制/RGB代码                 |
| background-image      | 背景图片       | url(图片路径)                                  |
| background-repeat     | 是否平铺       | repea/no-repeat/repeat-x/repeat-y             |
| background-position   | 背景位置       | lenght/position 分别是x和y坐标                 |
| background-attachment | 背景附着       | scroll(背景滚动)  /fixed(背景固定)             |
| 背景简写               | 书写更简单     | 背景颜色 背景图片 背景平铺 背景滚动 背景位置    |
| 背景色半透明           | 背景颜色半透明 | background: rgba(0，0，0, 0.3); 后面必须是4个值 |


```
    <head>
        <style>
            .nav a {
                display: inline-block;
                width: 120px;
                height: 58px;
                background-color: pink;
                text-align: center;
                line-height: 58px;
                color: #fff;
                text-decoration: none;
            }
            .nav .bg1 {
                background: url(images/bg1.png) no-repeat;
            }
            .nav .bg1:hover {
                background-image: url(images/bg11.png);
            }
        </style>
    </head>
    <body>
        <div class="nav">
            <a href='#'>五彩导航</a>
            <a href='#'>五彩导航</a>
            <a href='#'>五彩导航</a>
            <a href='#'>五彩导航</a>
            <a href='#'>五彩导航</a>
        </div>
    </body>
```

css的三大特性
css有三个非常重要的三个特性, 层叠性, 继承性, 优先级

1.1 层叠性
相同选择器给设置相同的样式, 此时一个样式就会覆盖(层叠)另一个冲突的样式,
层叠性主要解决样式冲突的问题

```
    <head>
        <style>
            div {
                color: red;
            }
            div {
                color: pink;
            }
        </style>
    </head>
    <body>
        <div> 长江后浪推前浪</div>
    </body>
```

层叠性原则:
样式冲突, 遵循的原则是就近原则, 哪个样式离结构近, 就执行哪个样式
样式不冲突, 不会层叠

1.2 继承性
现实中的继承, 我们继承了父亲的姓
css中的继承, 子标签会继承父标签的某些样式, 如文本颜色和色号,
简单的理解就是, 子承父业

恰当地使用集成可以简化代码, 降低css样式的复杂性
子元素可以集成父元素的样式(text, font, line 这些元素开头的可以继承, 以及color属性)

```
    <head>
        <style>
            div {
                color: pink;
                font-size: 14px;
            }
        </style>
    </head>
    <body>
        <div>
            <p>龙生龙, 凤生凤 </p>
        </div>
    </body>
```

`<div>`和`<p>`可以继成`<body>`

```
    <head>
        <style>
            body {
                color: pink;
                font: 12px/24px 'Microsoft Yahei';
            }
            div {
                /* 子元素继承了父元素的body的行高1.5 */
                /* 这个1.5 就是当前元素文字大小的 font-size的1.5倍 */
                font-size: 14px;
            }
            p {
                /* 1.5 * 16 = 24 当前的行高*/
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <div>粉红色的回忆</div>
        <p> 分红色的回忆</div>
    </body>
```

```
    font: 12px/1.5 'Microsoft Yahei';
```

1.3 优先级
当同一个元素指定多个选择器, 就会有优先级的产生
选择器相同, 则执行层叠性
选择器不同, 则根据选择器权重执行

选择器权重如下表所示

|        选择器        | 选择器权重 |
| ------------------- | ---------- |
| 继承 或者 *          | 0，0，0，0   |
| 元素选择器           | 0，0，0，1   |
| 类选择器, 伪类选择器 | 0，0，1，0   |
| id选择器             | 0，1，0，0   |
| 行内样式 style=""    | 1，0，0，0   |
| !important 重要的    | 无穷大     |

```
    <head>
        <style>
            .test {
                color: red;
            }
            div {
                color: pink;
            }
            #demon {
                color: green;
            }
        </style>
    </head>
    <body>
        <div class="test" id="demon" style="color: purple"> 你笑起来真好看</div>
    </body>
```

优先级注意点:
1, 权重是有4组数字组成, 但是不会有进位
2, 可以理解为类选择器永远大于元素选择器, id选择器永远大于类选择器, 以此类推
3, 等级判断从左向右, 如果某一位数值相同, 则判断下一位数值
4, 可以简单记忆法, 通配符和继承权重为0, 标签选择器为1, 类(伪装)选择器为10, id选择器为100, 行内样式表为1000
!important 无穷大
5, 继承的权重是0, 如果该元素没有直接选中, 不管父元素权重多个, 子元素得到的权重都是0

```
    <head>
        <style>
            #father {
                color: #red;
            }
            /* p继承的权重为0 */
            /* 所以以后我们看标签到底执行哪个样式, 就先看这个标签有没有直接被选出来 */
            p {
                color: pink;
            }
            body {
                color: red;
            }
            a {
                color: green;
            }
        </style>
    </head>
    <body>
        <div id="father">
            <p>你还是很好看</p>
        </div>
        <a href="#"> 我是单独的样式 </a>
    </body>
```

权重叠加: 如果是复合选择器, 则会有权重叠加, 需要计算权重

```
    <head>
        <style>
            /* li的权重就是0，0，0，1 */
            li {
                color: red;
            }
            ul li {
                color: green;
            }
            .nav li {
                color： pink;
            }
        </style>
    </head>
    <body>
        <ul>
            <li>大猪蹄子</li>
            <li>大肘子</li>
            <li>猪尾巴</li>
        </ul>
    </body>
```

```
    div ul li ---> 0,0,0,3
    .nav ul li ---> 0,0,1,2
    a:hover ---> 0,0,1,1
    .nav a ---> 0,0,1,1
```


