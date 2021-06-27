前端:
1, HTML
- 标签, 这个标签只要能记住这个标签怎么写, 是什么效果就可以了, 如果可以记20个标签, 90%以上的网站都可以写了, 这20个标签是经常会用到的

2, CSS
- 效果, color: 
	color: red;
	
3, JavaScript
- 稍微会多些内容(语言基础:数据类型, 数据类型提供了哪些方法等)
- 效果, 先查找, 然后操作

所有公司的服务器, 比如nginx等, 本质上都是写了个socket, 然后如果我的本地有个客户端, 

我在我的浏览器上, 我的浏览器就是一个socket客户端, 

4, jQuery
相当于是javascript的一个类库

html & css & javascript, 学会了前端的东西就算学会了,它是前端的三把利器
html 相当于赤裸裸的人, 
css 相当于给他穿上各种华丽的衣服
javascript 不再让这个人是个静态的人,而是让这个人可以动起来

javascript 和 java之间一点关系都没有, 可能只是名字上相似而已
javascript 和 python一样是一门编程语言, 只不过这门编程语言是在浏览器上给大家看的

	<!DOCTYPE html>

DOCTYPE 告诉浏览器按照什么规则解析你的标签

	<meta charset="UTF-8">
	<!--自闭合标签-->

	<meta http-equiv="content-type" content="text/html;charset=utf-8">
	<meta charset="UTF-8">
	<!--页面编码(告诉浏览器是什么编码)-->

	<meta http-equiv="Refresh" Content="30">
	<!--刷新和跳转,30秒刷新一次-->
	<meta http-equit="Refresh" Content="5; Url=http://www.autohome.com.cn">
	<!--刷新和跳转-->

	<meta name="keywords" content="星际">

	<meta http-equit="X-UA-Compatible" content="IE=edge">
	<!--兼容IE-->

我下面出现的效果都是用utf-8编码,让浏览器去解释


[title标签]
标题信息, name="html"叫做标签的属性

	<title name="html"> </title>

[link标签]
引入CSS
	<link rel="stylesheet" type="text/css" href="css/common.css">
---	
引入icon
	<linke rel="shorecut icon" href="image/favicon.ico">


DIV自身没有什么效果, 
我们加CSS,就是为了给它添加效果, 相当于我给你提供一个标签, 这个标签它的自身的功能特别的少,
我通过css就可以给它附件很多的功能, 这个功能我想让它变成就什么,就可以变成什么, 所以才叫div+css

[span标签]

在html里面, 我们用到的标签分成了两大类, 
- 块标签, 自己就占用一行
	<div> <hl> <p>
- 内联标签, 我内容有多少, 我就占用多少
	<a> <span> <select>

"<" 可以写成&lt;
在html里面特殊的符号, 是由特殊的代码来做展示的

[p标签]
表示是一个段落
	<p>asdfasdf</p>
p标签的段落之间的空白有点多, 这是因为<P>标签默认有一个自己多占用的行,除了内容本身,额外又多占用了一些, 段落和段落之间有些间距

[br标签]
换行标签,自闭合标签
	<br/>

[a标签]
有特殊的属性叫做href
	<a href="http://www.baidu.com">xx</a>

启用新的tag页进行跳转
	<a href="http://www.baidu.com" target="_blank">xx</a>

[锚点]
	<a href="#i1">第一章</a>
	<!--跳转到id=i1那里-->
	<a href="#i2">第二章</a>
	<a href="#i3">第三章</a>
	
	<div id="i1"  style="height: 500px"> 第一章内容 </div>
	<div id="i2"  style="height: 500px"> 第二章内容 </div>
	<div id="i3"  style="height: 500px"> 第三章内容 </div>