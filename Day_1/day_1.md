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

```
<!DOCTYPE html>
```

DOCTYPE 告诉浏览器按照什么规则解析你的标签

```
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
```

我下面出现的效果都是用utf-8编码,让浏览器去解释


**[title标签]**

标题信息, name="html"叫做标签的属性

```
<title name="html"> </title>
```

**[link标签]**

引入CSS

```
<link rel="stylesheet" type="text/css" href="css/common.css">

```



引入icon

```
<linke rel="shorecut icon" href="image/favicon.ico">
```


DIV自身没有什么效果, 
我们加CSS,就是为了给它添加效果, 相当于我给你提供一个标签, 这个标签它的自身的功能特别的少,
我通过css就可以给它附件很多的功能, 这个功能我想让它变成就什么,就可以变成什么, 所以才叫div+css

**[span标签]**

在html里面, 我们用到的标签分成了两大类, 
- 块标签, 自己就占用一行

```
`<div> <hl> <p>`
```

```
<body>
    <h1>标题标签</h1>
    <h1>标题一共六级选</h1>
    <h2>文件加粗一行显</h2>
    <h3>由大到小依次减</h3>
    <h4>从中到轻随之变</h4>
    <h5>语法规范书写后</h5>
    <h6>具体效果刷新见</h6>
</body>
```

- 内联标签, 我内容有多少, 我就占用多少

```
`<a> <span> <select>`
```

--

#"<" 可以写成 '&lt;'

#在html里面特殊的符号, 是由特殊的代码来做展示的

--

**[p标签]**

表示是一个段落

```
<p>asdfasdf</p>
```

p标签的段落之间的空白有点多, 这是因为<P>标签默认有一个自己多占用的行,除了内容本身,额外又多占用了一些, 段落和段落之间有些间距
要写几个段落就用几个段落标签

**[br标签]**

换行标签,自闭合标签
在代码中, 要显示的内容中输入回车键是没有任何作用的, 除非让他遇到我们<br />标签

```
<br/>
```
```
<body>
    <h1>圣诞节的那些事</h1>
    1, 圣诞节是怎么由来的 <br />
    2, 圣诞老人的由来 <br />
    3, 圣诞树的由于 <br />
</body>
```



```
<body>
    我是<strong>加粗</strong>的文字
    我是<b>加粗</b>的文字
    我是<em>倾斜</em>的文字
    我是<i>倾斜</i>的文字
    我是<del>删除线</del>
    我是<s>删除线</s>
    我是<ins>下划线</ins>
    我是<u>下划线</ins>
</body>
```

**[a标签]**

有特殊的属性叫做href
a 是 anchor的缩写

```
<a href="http://www.baidu.com">xx</a>
```

**启用新的tag页进行跳转**

```
<a href="http://www.baidu.com" target="_blank">xx</a>

```

**内部链接**
```
<body>
    <a href="xx.html">公司简介</a>
</body>
```

**空连接**
当如果没有确定连接目标时,
```
<body>
<a href="#">首页</a>
</body>
```

**下载链接**
```
<body>
<a href="img.zip">首页</a>
</body>
```

**图片链接**
```
<body>
<a href="http://www.baidu.com"><img src="img.jpg"/></a>
</body>
```

**[锚点]**

```
<a href="#i1">第一章</a>
<!--跳转到id=i1那里-->
<a href="#i2">第二章</a>
<a href="#i3">第三章</a>

<div id="i1"  style="height: 500px"> 第一章内容 </div>
<div id="i2"  style="height: 500px"> 第二章内容 </div>
<div id="i3"  style="height: 500px"> 第三章内容 </div>
```

id也是不允许重复的

**[div标签]**

div标签最显著的特点就是一个人独占一行
div是division的缩写, 表示分割, 分区

span一行可以放好多好多个
span意为跨度, 跨距

```
<body>
    <div style="color: green;">
    	asdfasdf
        <div style="color: red;">
        <div>
        <a>asdf</a>
    		</div>
    	</div>
    </div>
</body>
```

**[特殊字符]**
| 描述    |    字符的代码     |
| --- | --- |
|  空格符   | `&nbsp;`    |


**[img标签]**

所谓属性: 简单理解就是属于这个图像标签的特性

```
<img src="图像URL" />
```

```

<body>
    <h4>图像标签的使用: </h4>
    <img src="img.jpg" />
    <h4> alt替换文本 图像显示不出来的时候用文字替换: </h4>
    <img src="img.jpg" alt="我是pink老师"/>
    <h4> title 提示文本 鼠标放到图像上, 提示的文字: </h4>
    <img src="img.jpg" alt="我是pink老师" title="我是pink老师思密达"/>
    <h4> width 给图像设定宽度:</h4>
    <img src="img.jpg" alt="我是pink老师" title="我是pink老师思密达" width="500">
    <h4> height 给图像设定高度:</h4>
    <img src="img.jpg" alt="我是pink老师" title="我是pink老师思密达" width="500" height="100" />
    <h4> border 给图像设定边框: </h4>
    <img src="img.jpg" alt="我是pink老师" title="我是pink老师思密达" width="500" height="100" border="15" />
</body>
```

当图片显示不出来的时候, 显示"我是pink老师"
title, 当鼠标放到图片上面去, 会显示文字信息

**目录文件夹:**
就是普通文件夹, 里面只不过存放了我们做页面所需要的相关素材, 比如html文件, 图片等等, 

**根目录:**
打开目录文件夹的第一层就是根目录


**[input标签 & select标签 & textarea & form]**

```
<body>
	<form>
		<div style="border: 1px solid red;">
		<p> 用户名: <input type="text"/> </p>
		<p> 密码: <input type="password"/> </p>
		<p> 性别: 
			<br /> 男 <input type="radio" name="gender" /> 
			<br /> 女 <input type="radio" name="gender"/> 
		</p> 
		<p> 爱好:
			<br /> 羽毛球 <input type="checkbox" />
			<br /> 吉他 <input type="checkbox" />
			<br /> 轮滑 <input type="checkbox" />			
		</p>
		<p> 城市:
			<select>
				<option> 北京 </option>
				<option> 上海 </option>
				<option> 广州 </option>
			</select>
			<select multiple size="10">
				<option> 北京 </option>
				<option> 上海 </option>
				<option> 广州 </option>
			</select>
			<select>
				<optgroup label="辽宁省">
					<option> 大连 </option>
					<option> 沈阳 </option>
				</optgroup>
				<optgroup label="江苏省">
					<option> 南京 </option>
					<option> 苏州 </option>
				</optgroup>
			</select>
		</p>
		<p>文件: 
			<input type="file"/>
		</p>
		<p>备注:
			<textarea></textarea>
		</p>
		<inpute type="submit" value="submit"/>
		<inpute type="button" value="button"/>
		<inpute type="reset" value="reset"/>
	</form>
</body>
```

只要name=gender 相同, 它俩就可以互斥了
size="10", 默认显示10个, 超过10个就给添加滚动条

inpute系列标签 type:
- text
- password
- radio
- checkbox
- file
- button(普通的按钮)
- submit(提交当前表单)
- reset(重置表单)

---

表单域(form)

|  属性   |  属性值   |                      作用                      |
| ------ | -------- | --------------------------------------------- |
| action | url地址   | 用于指定接收并处理表单数据的服务器程序的url地址    |
| method | get/post | 用于设置表单数据的提交方式, 其取值为get或post     |
| name   | 名称      | 用于指定表单的名称, 以区分同一个页面中的多个表单域 |


```
<body>
    <form action="htt://www.baidu.com" method="get">
    	<input type="text" />
    	<input type="submit" value="提交" />
    </form>
</body>
```

提交数据

对于raido,必须有相同的名字才可以多选一

input表单元素
| 属性    |   属性值  |  描述   |
| --- | --- | --- |
|  name   |   由用户自定义  | 定义input元素的名称    |
|  value   |    由用户自定义 |   规定input元素的值  |
|  checked   |     checked |   规定此input元素首次加载时应该被选中  |
|   maxlength  |  正整数   |    规定输入字段中的字符的最大长度  |

1, name 和value是每个表单元素都有的属性值, 主要给后台人员使用
2, name表单元素的名字, 要求单选按钮和复选框要有相同的name值
3, checked属性主要针对于单选按钮和复选框, 主要作用一打开页面,就要可以默认选中某个表单元素

```
<input type="radio" name="sex" value="男" checked="checked" /> 男
```

4, maxlength是用户可以在表单元素输入的最大字符数, 一般较少使用

    ```
    <form action="htt://www.baidu.com" method="POST" enctype="multipart/form-data">
    	<input type="text" name="user" vlaue="请输入密码" />
    	<input type="password" name="pwd" />
    	男 <input type="radio" name="gender" value="1"/>
    	女 <input type="radio" name="gender" value="2" />
		<p>爱好:
			篮球 <inpute name="favor" type="checkbox" value="1" />
			足球 <inpute name="favor" type="checkbox" value="2" />
			玻璃球 <inpute name="favor" type="checkbox" value="3" />
		</p>
		<P>文件:
			<input type="file" name="asdfasdf">
		</P>
		<p>
			<select name="city">
				<option value="1">北京</option>	
				<option value="2">上海</option>	
				<option value="3">广州</option>				
			</select>
		</p>
		<p>
			备注: <textarea name="extra"></textarea>
		</p>
    	<input type="submit" value="submit" />
    </form>
    ```

如果要上传文件的话,就必须要加上 enctype="multipart/form-data", 只有加上这个选项,文件才能源源不断的分块
上传到服务器端, 不然文件本身是无法上传到服务器端的

**[label标签]**

label标签作用不大, 只能说是在小细节方面帮你做一个用户体验的提升, 

**[ul ol dl标签]**
列表标签
表格是用来展示数据的, 那列表就是用来布局的
列表最的的特点就是整齐,整洁, 有序, 它作为布局会更加自由和方便

根据使用场景不同, 列表可以分为三大类, 无序列表(ul), 有序列表(ol), 自定义列表(dl)

ul默认加上前缀效果

1, 无序列表的各个列表项之间没有顺序级别之分, 是并列的
2, `<ul></ul>` 中只能嵌套,` <li></li>`, 直接在`<ul></ul>`标签中输入其它标签或文字的做法是不被允许的
3, `<li>`与`</li>` 之间相当于一个容器, 可以容纳所有元素
4, 无序列表会带有自己的样式属性, 但在实际使用时, 我们会使用css来设置

```
<ul>
    <li>asdfasdf</li>
    <li>asdfasdf</li>
    <li>asdfasdf</li>
</ul>
```

有序列表
1, `<ol></ol>`中只能嵌套`<li></li>`, 直接在`<ol></ol>`标签中输入其它标签或者文字的做法是不被允许的
2, `<li></li>` 之间相当于一个容器, 可以容纳所有元素
3, 有序列表会带有自己样式属性, 但在实际使用时, 我们会使用CSS来设置

```
<ol>
    <li>asdfasdf</li>
    <li>asdfasdf</li>
    <li>asdfasdf</li>
</ol>
```

自定义列表
自定列表的使用场景
自定义列表常用语对术语或名词进行解释和描述, 定义列表的列表项没有任何项目符号

1, `<dl></dl>` 里面只能包含`<dt>和<dd>`
2, `<dt>`和`<dd>`个数没有限制, 经常是一个`<dt>`对应多个`<dd>`

```
<dl>
    <dt>asdfasdf</dt>
    <dd>asdfasdf</dd>
    <dd>asdfasdf</dd>
</dl>
```

**[table标签]**
表格不是用来布局页面的, 而是用来展示数据的
合并单元格 rowspan, colspan

```
<body>
    <table border="1">
    	<thead>
			<tr>
				<td colspan="2">第一列</td>
				#colspan 这个标签占用2个空格
				<td>第二列</td>
				<td>第三列</td>
			</tr>
		</thead>
    	<tbody>
			<tr>
				<td>第一列</td>
				<td rowspan="2">第二列</td>
				<td>第三列</td>
			</tr>
		</tbody>
    </table>
</body>
```

align="center"不推荐使用这个方法, 建议使用css方法来实现
```
<body>
    <table align="center">
        <tr> <th>姓名</th> <th>性别</th> <th>年龄</th> </tr>
        <tr> <td>刘德华</td> <td>男</td> <td>56</td> </tr>
    </table>
</body>
```

|    属性名    |        属性值        |                    描述                    |
| ----------- | ------------------- | ------------------------------------------ |
| align       | left, center, right | 规定表格相对周围元素的对齐方式                |
| border      | 1 或 ""              | 规定表格单元是否拥有边框，默认为"",表示没有边框 |
| cellpadding | 像素值               | 规定单元边沿与其内容之间的空白,默认1像素       |
| cellspacing | 像素值               | 规定单元格之间的空白,默认2像素                |
| width       | 像素值               | 规定表格的宽度                               |


**[fieldset标签]**


**[iframe标签]**

    <iframe style="width: 100%; height: 2000px;" src="http://autohome.com.cn"></iframe>

src写上哪个网址, 相当于把那个网址的东西放到你这框里展示出来了, 其实就这么个功能, 
对于真实的可用iframe做什么, 上传文件或跨域的时候会涉及到它
