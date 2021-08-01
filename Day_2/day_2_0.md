css其实叫做层叠样式表, 在ps中有图层的概念, 其实在css中也有图层的概念
默认情况下, 我们看到的页面只有一层, 其实是可以分多层的, 如果说第一层是不透明的
只能看第一层, 第一层如果透明, 第一层和第二册都可以看到的, 全部都透明, 全部都可以看到的, 写css的时候也是可以这样的, 可以人为的创造出很多层来, 也可以人为的让你做
操作, 到底是否透明都是可以做的, 

从它的学名上它叫做层叠样式表, 从最通俗的语言上来说这东西就是给一个标签加上样式,
加上样式相当于给它穿上衣服, 穿上衣服看起来就好看些了, 

如何给东西加样式了, 

```
/* 选择器 {样式} */
/* 给谁修改样式 {修改什么样式} */
```

```
h1 { color: red;  font-size:25px; }
选择器 { 属性: 值; 属性:值; }
```

CSS是专门为标签加样式的,

	<head>
		<meta charset="UTF-8">
		<title></title>
		<style>
			div{
				background-color: red;
				corlor: white;
			}
		</style>
		<!--style写在这里表示在当前页面中都适用-->
	</head>
    <body>
    	<div style="background-color: red; color: black;">88</div>
		<div> 99 </div>
		<!--这里就会应用在head中定义的样式-->
    </body>

css还可以专门放在一个文件中, 在css文件中
css文件:

	div {
		background-color: red;
		color: white;
	}

css代码风格
1, 紧凑格式
```
h3 { color: deeppink; font-size: 20px; }
```
2, 展开格式(推荐)
```
h3 {
    color: pink;
    font-size: 20px;
    /* 标题便签比较特殊,需要单独指定文字大小*/
}
```

css 使用font-size属性定义字体大小
px(像素) 大小是我们网页的最常用的单位
谷歌浏览器默认的文字大小为16px
不同浏览器可能默认显示的字号大小不一致, 我们尽量给一个明确值大小, 不要默认大小
可以给body指定整个文字的大小

选择器分类,
选择器分为: 基础选择器和复合选择器两大类，
基础选择器是由 单个选择器组成的
基础选择器又包括: 标签选择器, 类选择器， id选择器 和 通配符选择器

语法
```
标签名 {
    属性1: 属性值1;
    属性2: 属性值2；
    属性3: 属性值3;
    ...
}
```

```
<head>
    <style>
        p {
            color: green;
        }
        div {
            color: pink;
        }
    </style>
</head>
<body>
    <p>男生</p>
    <p>男生</p>
    <p>男生</p>
    <div>女生</div>
    <div>女生</div>
    <div>女生</div>
</body>

```

---

    <head>
    	<link rel="stylesheet" href="common.css">
		<!--导入css文件-->
    </head>

---

**标签选择器**
1, 作用
   标签选择器可以把某一类标签全都选择出来,比如所有<div>标签和所有的<span>标签
2, 优点
   能快速为页面中同类型的标签统一设置样式
3, 缺点
   不能设计差异化样式, 只能选择全部的当前标签

**类选择器**
如果想要差异化选择不同的标签, 单独选一个或某几个标签,  可以使用类选择器
语法

```
.类名字 {
    属性1:  属性值1;
    ...
}
```
```
<style>
    .red {
        color: red;
        width: 100px;
        height: 100px;
        /* 背景颜色 */
        background-color: red;
    }
    .green {
        width: 100px;
        height: 100px;
        background-color: green;
    }
</style>

<body>
    <div class='red'> 变红色 </div>
</body>
```

```
<style>
    .box {
        /*公共样式可以放到box里面*/
        width: 100px;
        height: 100px;
    }
    .red {
        background-color: red;
    }
    .green {
        background-color: green;
    }
</style>
<body>
    <div class="box red"> 红色 </div>
    <div class="box greend"> 绿色 </div>
</body>
```


/* 类选择器口诀: 样式点定义, 结构类(class)调用, 一个或多个 开发最常用*/

谁想使用谁就加个类的名字,来调用就可以了,类的名字前面就不要在加点了, 这个点就自动变成了class
一个或多个, 你不光可以给一个标签来定义类名, 还可以给多个标签都来调用这个类名
在开发过程当中, 类选择器是最常用的, 需要重点掌握的


类选择器,
注意:
1, 类选择器使用"."(英文符号)进行标识, 后面紧跟类名(自定义, 我们自己命名的)
2, 可以理解为给这个标签起了一个名字,来表示
3, 长名称或词组可以使用中横线来为选择器命名
4, 不要使用纯数字, 中文等命名, 尽量使用英文字母来表示
5, 命名要有意义, 尽量使用别人一眼就知道这个类名的目的

多类名使用方式

```
<div class="red font20"> 亚瑟 </div>
/* 包含了两个类名 red 和 font20 */
```

1, 在标签class属性中写多个类名
2, 多个类名中间必须空格分开
3, 这个标签就可以分别具有这些类名的样式
4, 从而节省css代码, 统一修改也非常方便
5, 多类名选择器在后期布局也比较复杂的情况下, 还是较多使用的


id选择器
id选择器的口诀
样式是通过#来定义的, 结构是通过id来调用的, 只能调用一次, 别人切勿使用

id选择器和类选择器的区别
1, 类选择器(class) 好比别人的名字, 一个人可以有多个名字, 同时一个名字也可以被多个人使用
2, id选择器好比人的身份证号码, 全中国是唯一的, 不得重复
3, id选择器和类选择器最大的不同就是在于使用次数上
4, 类选择器在修改样式中用的是最多的, id选择器一般用于页面唯一性的元素上, 经常和JavaScript搭配使用

通配符选择器
在css中, 通配符选择器使用 "*"定义, 它表示选取页面中所有元素(标签)
它选就是选择所有的, 里面写什么样式，就会给所有的标签都加上这种样式,
把我们html, body, div, span, li等等标签都改为了红色,
通配符选择器不需要调用, 自动就给所有的元素使用样式

语法
```
*  {
    属性1: 属性值1;
    ...
}
```

```
<head>
    <style>
        #pink {
            color: pink;
       }
    </style>
</head>
<body>
    <div id="pink"> 迈克尔，杰克逊</div>
    /* 这里调用了, pink, 后面就不能再调用pink了 */
</body>
```

|  基础选择器  |           作用           |               特点                |   使用情况   |         用法         |
| ----------- | ------------------------ | --------------------------------- | ------------ | -------------------- |
| 标签选择器   | 可以选出所有的标签, 比如P | 不能差异化选择                    | 较多         | p { color: red; }    |
| 类选择器     | 可以选出1个或者多个标签   | 可以根据需求选择                  | 非常多       | .nav { color: red; } |
| id选择器     | 一次只能选择一个标签      | id属性只能在每个html文档中出现一次 | 一般和js搭配 | #nav {color: red; }  |
| 通配符选择器 | 选择所有的标签            | 选择的太多, 有部分不需要           | 特殊情况使用 | * { color: red; }    |

css的存放位置
1, 单独的css文件 //优先级最低的
2, html的head部分
3, 标签的属性上 //优先级是最高的

1, 行内样式表(行内式)
```
<div style="color: red; font-size: 12px;">青春不常在, 抓紧谈恋爱</div>
```
style其实就是标签的属性
在双引号中间, 写法要符合css规范
可以控制当前的标签设置样式
由于书写繁琐, 并且没有体现出结构与样式相分离的思想, 所以不推荐大量使用, 只有对当前元素添加简单样式的时候,可以考虑使用
使用行内样式表设定css, 通常也被称为行内式引入

2, 内部样式表(嵌入式)
是写到html页面内部, 是将所有的css代码抽取出来, 单独放到一个`<style>`标签中
通过这种方式可以方便控制整个页面中的元素样式设置
代码结构清晰, 但是并没有实现结构与样式完全分离
使用内部样式表设定css, 通常也被称为嵌入式引入, 这种方式是我们练习时常用的方式

3, 外部样式表(链接式)
实际开发都是外部样式表, 适合于样式比较多的情况， 核心是: 样式单独写到css文件中, 之后把css文件引入到html页面中使用
引入外部样式表分为两步:
3.1 新建一个后缀名为.css的样式文件, 把所有css代码都放入此文件中(这个css文件中只有样式, 没有标签)
3.2 在html页面中, 使用`<link>`标签引入这个文件

```
style.css ==>
div {
    color: pink;
}
```

```
<head>
    <link rel="stylesheet" href="css文件路径">
</head>
```

|   样式表   |          优点          |     缺点     |   使用情况    |   控制范围   |
| --------- | ---------------------- | ----------- | ------------ | ----------- |
| 行内样式表 | 书写方便,权重高         | 结构样式混写 | 较少          | 控制一个标签 |
| 内部样式表 | 部分结构和样式相分离     | 没有彻底分离 | 较多          | 控制一个页面 |
| 外部样式表 | 完全实现结构和样式相分离 | 需要引入     | 最多,吐血推荐 | 控制一个页面 |

如果是相同的属性,

---
    <head>
	    <style>
	    	div {
	    		color: green;
				/* 找到所有的div */
	    	}
	    	#i1 {
	    		front-size: 32px;
				color: green;
				/* 这里是注释 */
	    	}
	    	<!--#i1, 我要去找id为i1的标签-->
			.c1 {
				/*找所有的标签, 如果你的标签有个class属性是c1, 不管你是什么标签*/
				/*它都要给我应用这个样式*/
			}
			/*层级选择器*/
			.c2 div p a {
				/* .c2/div/p/a */
				
			}
			.c2 div p .c3 {
				/* .c2/div/p/a */
				
			}
			/*组合选择器*/
			
			.c4,.c5,.c6 {
				/*只写一份就可以了*/	
			}
			
			.c5 {
	
			}

			.c6 {

			}

	    </style>
    </head>
    <body>s
		<div class="c4"> 1 </div>
		<div class="c5"> 2 </div>
		<div class="c6"> 3 </div>

    	<a id="i1">baidu</a>
		<span class="c1">1</span>
		<a class="c1">3</a>

		<div class="c2">
			<div></div>
			<div>
				<p>
					<span>00</span>
					<a class="c3">uu</a>
				</p>
			</div>
    </body>

在html标签里面id是不可以重复的, #i1这么写, 只找到一个为它加上样式
但是class是可以重复的, 并且.c1也是用过最多的方式

    <html>
    <head>
    	<meta charset="UTF-8">
    	<title></title>
    	<style>
    		.c1{
    			color: red;
    			background-color: aqua;
				background-color: #ddd;
				background-color: rgb(0,0,0);
				/* 也可以通过RGB的形式来写 */
    			front-size: 32px;
				height: 50px;
				width: 100%;
				/*宽度和高度就是设置当前div的宽度和高度的*/
				/*宽度是有100%的, 高度是没有100%的*/
    		}
    	</style>
    </head>
    <body>
    	<div class="c1">asdfasdf</div>
		<div style="width: 500px">
			<div style="width: 20%; background-color: antiquewhite; float: left">asdf</div>
			/*相对于500来说占用 20%*/
			<div style="width: 80%; background-color: palegodenrod; float: left">asdf</div>
			/*相对于500来说占用 80%*/		
		</div>
    </body>
    </html>

<div>是块级标签, 默认是占一整行的

---

	<head>
		<meta charset="UTF-8">
		<title></title>
		<style>
			.img{
				background-image: url("4.gif");
				background-repeat: no-repeat;
				background-position: 0px;
				border-top-color: red;
				border-top-style: red;
				border-top-width: 4px;
				height: 50px;
				width: 200px;
				display: none;
				visibility: hidden;
			}
			.img2{
				background-image: url("4.gif");
				height: 20px;
				width: 20px;
			}
		</style>
	</head>
	<body>
		<div class="img"></div>
		<div class="img2"></div>
	</body>

这个div没高度,没宽度,加背景色其实是看不到的
如果我挖的洞特别大的话, 那它不是给你铺满而是一直放
默认情况下, 都是这样来搞的, 
background-repeat, 表示我不重复给你显示, 不论你这个洞挖多大, 该显示什么样, 就显示什么样, 
background-position, 显示图片的位置
border-top-color, 上边框是什么样式的
border-top-style, 上边框是什么类型的
border-top-width, 
display, 把哪个标签隐藏起来, 让位置消失
display: inline, 把块级标签变成内联标签
display: block, 变成块级标签
visibility, 只是让内容消失, 位置还在

---

css字体属性
css使用font-family属性定义文本的字体系列

各种字体之间必须使用英文状态下的逗号隔开,
一般情况下, 如果有空格隔开的多个单词组成的字体, 加引号,
尽量使用系统默认自带字体, 保证在任何用户的浏览器中都能正确显示

```
p { font-family: "微软雅黑"; }
div { font-family: Arial, "Microsoft Yahei", "微软雅黑"; }
```

<head>
    <style>
        h2 {
            font-family: "宋体";
        }
        p {
            font-family: "微软雅黑";
        }
    </style>
</head>
<body>
    <h2> pink的秘密</h2>
    <p> 那一抹众人中最漂亮的颜色 </p>
    <p> 优雅, 淡然, 又那么心中清澈 </p>
</body>


```
    <head>
    	<meta charset="UTF-8">
    	<title></title>
    </head>
    <body>
    	<span style="background-color: red; height: 50px; width: 200px;">asdfasdf</span>
		<span style="display:inline-block; height: 50px; background-color: red;"></span>
    </body>
```

```
.bold {
    font-weight: bold;
}
```
font-weight: normal | bold | bolder |  lighter | <number>

|  属性值  |                           描述                           |
| ------- | ------------------------------------------------------- |
| normal  | 默认值(不加粗)                                            |
| bold    | 定义粗体(加粗的)                                          |
| 100-900 | 400 等同于normal, 而700等同于bold, 注意这个数字后面不跟单位 |


```
p {
    font-style: normal;
}
```

font-style: italic
/* 字体倾斜 */

| 属性值  |                         作用                         |
| ------ | ---------------------------------------------------- |
| normal | 默认值, 浏览器会显示标准的字体样式, font-style: normal; |
| italic | 浏览器会显示斜体的字体样式                              |

```
body {
    font: font-style  font-weight   font-size/line-height   font-family;
    /* 不可以随便点到顺序 */
    font: italic   700   16px   'Microsoft yahei';
    /* 使用font属性时, 必须按上面语法格式中的顺序书写, 不能更换顺序, 并且各个属性间以空格隔开 */
    /* 不需要设置的属性可以省略(取默认值), 但必须保留font-size 和 font-family, 否则font属性将不起作用*/
}
```

```
div {
    text-align: center;
}
```

| 属性值  |      解释      |
| ------ | ------------- |
| left   | 左对齐(默认值) |
| right  | 右对齐         |
| center | 居中对齐       |


装饰文本
`text-decoration`属性规定添加到文本的修改, 可以给文本添加下划线, 删除线， 上划线等

```
div {
    text-decoration: underline;
}
```

|    属性值     |            描述             |
| ------------ | --------------------------- |
| none         | 默认,没有装饰线(最常用)       |
| underline    | 下划线, 链接a自带下划线(常用) |
| overline     | 上划线(几乎不用)             |
| line-through | 删除线(不常用)               |


纯内联标签它的高度和宽度都不生效,
块级标签可以写高度和宽度,
inline-block, 具有内联标签的属性, 又具有块标签的属性

    <span style="cursor: pointer;">pointer</span>
    <span style="cursor: help;">help</span>
    <span style="cursor: wait;">wait</span>
    <span style="cursor: move;">move</span>
    <span style="cursor: crosshair;">crosshair</span>

`text-indent` 属性用来指定文本的第一行的缩进, 通常是将段落的首行缩进

```
div {
    text-indent: 10px;
    text-indent: -20px;
    / *如果是负值 往左边移动 */
}
```

```
p {
    text-indent: 2em;
    /* 如果此时写了2em, 则是当前元素2个文字大小的距离 */
}
```

行间距
`line-height`属性用于设置行间的距离(行高), 可以控制文字行与行之间的距离
行间距, 包含了上间距, 文本高度, 下间距

```
p {
    line-height: 26px;
}
```

```
<style>
    div {
        line-height: 16px;
    }
</style>
```


---


边距(内边距, 外边距)
我们写上一个标签之后, 我们可以在这个标签的外部加点内容, 内部在加点内容
默认情况下, 写标签都是从左向右堆积, 

    <div style="height: 70px; border: 1px solid red;">
		<div style="height: 30px; background-color: green; 	margin-top: 27px; padding-top: 19px;"></div>
	</div>

margin 外边距, 本身不增加
padding 上边距, 本身增加

    <div style="height: 100px">
    	<div style="margin-top: 30px; margin-left: 100px;">
    		<input />
    		<input />
    		<input />
    	</div>
    </div>

---

    <body>
    	<div style="width: 500px;">
			<div style="width: 20px; background-color: aqua; float: left">g</div>
			<div style="width: 80px; background-color: beige; float: left">a</div>
			<div style="clear: both;"></div>
		</div>
    </body>

---
默认是一个标签占一行,但是如果漂浮标签, 就会跑到一行去
如果第一个标签占用20%, 第二个标签占用90%, 就超过了100%, 第二个标签,就会飘到第二行

position:
1, relative, 往往这个选项是和absolute结合着使用的
2, absolute, 虽然是按你的窗口固定在那个位置, 但是我去拉动这个文档的时候, 位置照样会变, 就不能永远固定在那个位置了
3, fixed 固定, 相对于浏览器的窗口, 想固定哪里就固定哪里
    
    <body>
    	<div style="height: 1000px; background-color: #ddd;"></div>
		<div style="position: fixed;">返回顶部</div>
		<!--将会固定在某个位置-->
		<div style="position: fixed; top:0px;">返回顶部</div>
		<!--将会固定在顶部-->
    </body>

---

    <body>
    	<div style="height: 500px; width: 400px; border: 1px solid red; position: relative;">
			<div style="position: absolute; bottom: 0; right: 0">111</div>
    	</div>
    </body>
    

---

Emmet语法
Emmet语法的前身是Zencoding它使用缩写,来提高html/css的缩写速度, vscode内部已经集成该语法
1, 快速生成html结构语法

1.1 生成标签, 直接输入标签名按Tab键即可, 比如, div 然后tab键, 就可以生成`<div></div>`
```
！ + Tab 键,可以生成代码结构
```

```
table + Tab键, 也可以生成结构
```
1.2 如果想要生成多个相同的标签, 加上 * 就可以了 比如 div * 3 ,就可以快速生成3个div

```
div*10, 中间不能有空格, 不然没有效果
```

1.3 如果有父子级关系的标签, 可以用 `>` 比如 `ul > li` 就可以了

```
ul>li
```

1.4 如果兄弟关系的标签, 用 + 就可以了, 比如 `div+p`

1.5 如果生成带有类名或者id名字的, 直接写 `.demo` 或则 `#two tab键`就可以了
`p.one`, 给p标签加了一个`class=one`的样式

1.6 如果生成的div类名是有顺序的, 可以自增符号 $

```
.demo$*5
```

```
<div class="demo"></div>
<div class="demo1"></div>
<div class="demo2"></div>
<div class="demo3"></div>
<div class="demo4"></div>
<div class="demo5"></div>
```
file:///D:/Git_Data/Git_Hub/Python/english/开言英语/U02-2.md
1.7 如果想要在生成的标签内些内容可以用 {} 表示
```
div{pink}
```
```
<div>pink</div>
```file:///D:/Git_Data/Git_Hub/Python/english/开言英语/U02-2.md

2, 快速生成css样式语法



CSS的复合选择器
1.1 在css中,可以根据选择器的类型把选择器分为 基础选择器 和 复合选择器,  复合选择器是建立在基础选择器之上, 对
基础选择器进行组合形成的

1) 复合选择器可以更准确、更高效的选择目标元素(标签)
2) 复合选择器是由两个或多个基础选择器, 通过不同的方式组合而成的
3) 常用的复合选择器包括, 后代选择器、子选择器、并集选择器、伪类选择器等等

1.2 后代选择器

可以一层一层向下去查找

```
    <head>
        <style>
            /* 我想要把ol里面的小li选出来改为pink */
            ol li {
                color: pink;
            }
            ol li a {
                color: red;
            }
            .nav li a {
                color: yellow;
            }
        </style>
    </head>

    <body>
        <ol>
            <li> 我是ol的孩子 </li>
            <li> 我是ol的孩子 </li>
            <li> 我是ol的孩子 </li>
            <li> <a href="#"> 它是孙子</a></li>
    </ol>
    <ul class="nav">
            <li> 我是ul的孩子</li>
            <li> 我是ul的孩子</li>
            <li> 我是ul的孩子</li>
            <li> <a href="#"> 不会变化的</a></li>
    </ul>
    </body>
```

1.3 子选择器
子元素选择器(子选择器) 只能选择作为某元素的最近一级子元素, 简单理解就是选亲儿子的元素

```
语法:
元素1 > 元素2 { 样式声明 }
```

上述语法表示选择元素里面的所有直接后代(子元素)元素2

元素1 和 元素2 中间用 大于号 隔开
元素1 是父级， 元素2 是子级, 最终选择的是元素2
元素2必须是亲儿子, 其孙子, 重孙之类都不归他管, 你可以叫他亲儿子选择器