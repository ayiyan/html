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
}
```

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

纯内联标签它的高度和宽度都不生效,
块级标签可以写高度和宽度,
inline-block, 具有内联标签的属性, 又具有块标签的属性

    <span style="cursor: pointer;">pointer</span>
    <span style="cursor: help;">help</span>
    <span style="cursor: wait;">wait</span>
    <span style="cursor: move;">move</span>
    <span style="cursor: crosshair;">crosshair</span>
   
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