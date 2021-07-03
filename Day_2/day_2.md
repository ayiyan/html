css其实叫做层叠样式表, 在ps中有图层的概念, 其实在css中也有图层的概念
默认情况下, 我们看到的页面只有一层, 其实是可以分多层的, 如果说第一层是不透明的
只能看第一层, 第一层如果透明, 第一层和第二册都可以看到的, 全部都透明, 全部都可以看到的, 写css的时候也是可以这样的, 可以人为的创造出很多层来, 也可以人为的让你做
操作, 到底是否透明都是可以做的, 

从它的学名上它叫做层叠样式表, 从最通俗的语言上来说这东西就是给一个标签加上样式,
加上样式相当于给它穿上衣服, 穿上衣服看起来就好看些了, 

如何给东西加样式了, 

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


---

    <head>
    	<link rel="stylesheet" href="common.css">
		<!--导入css文件-->
    </head>

---

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


