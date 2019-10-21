01.JS基础_JS简介

```javascript

```

#### 02.JS基础_JS的HelloWorld

```javascript

```

#### 03.JS基础_js编写位置

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title>111</title>
	<script>
	//借助window.onload 事件，在文档加载之后，进行相关操作
        //打开浏览器，所有资源加载完毕后。声明一个变量，变量名叫btn,文档加载获取多个对象的方法，方法名叫getEementsByTagName,获取button即第0个对象。btn这个方法是指，弹出一个弹出，弹出内容是获取这个对象的第一个属性和值。
	window.onload=function(){
		//获取按钮对应多元素节点对象
		var btn =document.getElementsByTagName("button")[0];
		//绑定单机响应函数
		btn.onclick =function(){
			//打印文本值
			alert(this.firstChild.nodeValue);
		}
	
	
	}
		
	</script>
	</head>
	<body>
		
		<button>click me!</button>
	</body>
</html>

```

alert:控制浏览器弹出一个警告框

document write :可以想body中输出一个内容

console.log():向控制台输出一个内容

JS语言从上到下执行，一行一行执行的

可以将js代码编写到标签的onclick属性中，当我们点击按钮时，js代码才会执行。

```javascript
<button onclick="alert('讨厌，你点我干嘛~~')；">点我一下<点我一下/button>
```

虽然可以写在标签的属性中，但是他们属于结构与行为耦合，不方便维护。不推荐使用。

可以将js代码写在超链接的href属性中，这样当点击超链接时，会执行js代码。

```javascript
<a href="javascript:alert('让您点您就点！！！');">你也点我一下</a>
<a href="javascript:;">你也点我一下</a>
```

可以将js代码编写到外部js文件中，然后通过script标签引入。(新建一个js,js文件名是：script.js)

写在外部文件中可以在不同的页面中同时引用，也可以利用浏览器的缓存机制，推荐使用的方式

```javascript
<script type="text/javascript" src="js/script.js"></script>
```

script标签一旦用于引入外部文件了，就不能在编写代码了，即使编写了浏览器也会忽略，

如果需要则可以在创建一个新的script标签于编写内部代码。

```javascript
<script type="text/javascript" src="js/script.js"></script>
<script type="text/javascript">
    alert("我是内容的js代码")
</script
```



#### 04.JS基础_基本语法

```;
alert("hello");    //弹窗
document.write("hello"); //页面内容
console.log("hello")； //控制台   该语句用来在控制台输出一个日志
```

/* 多行注释

多行注释，注释的内容不会被执行，但是可以在源代码中查看

要养成良好的编写注释的习惯，也可以通过注释来对代码进行一些简单的调试

*/



//单行注释，只对双斜杠后面的内容注释



1.js中严格执行大小写

2.js每一条语句以分号（；）结尾

--.如果不写分号，浏览器会自动添加，但是浏览器会消耗一些系统资源、

而且有些时候，浏览器会加错分号。所以在开发工作中，分号必须写。

3.js中会忽略多个空格和换行，所以我们可以利用空格和换行对代码进行格式化

#### 05.JS基础_字面量和变量

```javascript
//声明一个变量
//在js中使用var关键字来声明一个变量
var a;
console.log('a');
```

字面量（常量）：

都是一些不可改变的值

比如：1 2 3 4 5

字面量都是可以直接使用，但是我们一般都不会直接使用字面量



变量  变量可以用来保存字面量，而且变量的值是可以任意改变的

变量更加方便我们使用，所以在开发中都是通过变量去保存一个字面量，

而很少直接使用字面量



#### 06.JS基础_标识符

在js中所有的可以由我们自主命名的都可以称为是标识符

例如：变量名，函数名，属性名都属于标识符

命名一个标识符时需要遵守如下的规则：

1.标识符中可以含有字母，数字，_,$

2.标识符不能以数字开头

3.标识符不能是ES中的关键字或保留字

4.标识符一般都采用驼峰命名法

-首字母小写，每个单词的开头字母大写，其余字母小写

js底层保持标识符时实际上是采用的Unicode编码



#### 07.JS基础_字符串

数据类型指的就是字面量的类型，在JS中一共有六种数据类型

String      字符串

Number   数值

Boolean   布尔值

Null           空值

Undefined  未定义

Object         对象

其中String   Number Boolean Null Undefined  属于基本数据类型

而Object属于引用数据类型



String 字符串

在js中字符串需要使用引号引起来

使用双引号或单引号都可以，但是不要混着用。

```javascript
var str ="hello";
console.log(str);
//等于
var str ="hello";
console.log("hello");//如果hello不加引号，变成变量

var  str ='hello';
str ="我说：“今天天气真不错！”"//执行会报错，引号不能嵌套。
//单引号不能放单引号
str ='我说：“今天天气正好！”'；//可执行。
//在字符串中我们可使用\作为转义字符，
//当表示一些特殊符号时可以使用\进行转义

/*
\"  表示 “
\ ' 表示'
\ n 表示换行
\ t 制表符 空格 tab键
\\  表示 \  str="\\"等于\ ,\\\\等于\\,\\\\\\等于\\\;

*/

//输出字面量 字符串str
alert("str");
//输出变量
alert(str);
```





#### 08.JS基础_Number

 

```javascript
var str2 ="hello";
str2 ="你好"；
str3 =3;//声明同一个变量，只需要写一次var
var str3 ="1";
str3 ="2";//声明一个新的变量，当然需要重新写上var


alert("hello,你好")；
console.log("我就是不出来")；//代码从上到下执行，alert执行的时候您需要点击弹框才可以见到控制台打印“我就是不出来”的内容。

```

js中所有的数值都是nubmer类型

包括整数和浮点数（小数）

```
var a=123;
a =456;//执行出来就是456，后面的覆盖前面的。后面的有效
var b="123";这个是字符串；
```

可以使用一个运算符typeof 来检查一个变量的类型。

语法：typeof 变量

检查字符串时，会返回string

检查数值时，会返回number

console.log(typeof b);



```
number.max_value
js中可以表示的数字的最大值
Number.MAX_VALUE    1.7976931348623157e(科学记数法)
如果使用的number超过了最大值，则会返回一个infinity,表示正无穷
-infinity，表示负无穷。
a=Number.MAX_VALUE *Number.MAX_VALUE ;
console.log(a);//执行得到正无穷：infinity
使用typeof检查infinituy，也会返number
使用typeof检查NaN，也会返number
```

最小值number.min_value

在js中整数的运算基本可以保证精确

如果使用js进行浮点元素，可能得到一个不精确的结果。

所以千万不要使用js进行精确度要求比较高的计算。

#### 09.JS基础_布尔值

布尔值只有两个，主要用来做逻辑判断

true  真 

false  假



使用typeof检查一个布尔值时，会返回b oolean

var bool =true;

console.log(typeof bool);//执行：boolean

#### 10.JS基础_Null和Undefined

Null(空值)类型的值只有一个，就是null

null这个值专门用来表示一个为空的对象

使用typeof检查一个null值时，会返回object



var a =null;

console.log(typeof a);//返回object



Undefined（未定义）类型的值只有一个，就是undefind

当声明一个变量，但是并不给变量赋值时，他的值就是undefinde

使用typeof检查一个undefined时会返回undefined

var b;

console.log(b);//声明了一个变量，但是没有赋值，所以显示没有定义。



var b ="undefined";//声明一个变量，变量是字符串

console.log(b);  //返回string,所以要注意当声明一个变量的时候用到了双引号就是字符串类型。

#### 11.JS基础_强制类型转换-String

强制类型转换

指将一个数据类型强制转换为另一个数据类型

类型转换主要指，将其他的数据类型，转换为

String number boolean

将其他的数据类型转换为string

var  a=1232;

console.log(type);



方式一：调用被转换类型的toString()方法

该方法不会影响到原变量，他会将转换的结果返回。

但是注意，null和undefined这两个值没有toString的方法

如果调用他们的方法，会报错。

//调用a的tostring（）方法

//调用xxx的yyy()方法，就是xxx.yyy()

```javascript
var a =123;
var b =a.toString();
console.log(typeof b);
console.log(b);
//执行返回:"string" "123"

一样
 
var a =123;
a=a.toString();
console.log(typeof a);
console.log(a);
//执行返回:"string" "123"

a =true;
a=a.toString();
console.log(typeof a);
console.log(a);
//执行返回“string" "true"

a =true;
a=a.toString();
console.log(typeof a);
console.log(a);

a=null;
a=a.toString();//报错

a=undefined;
a=a.toString();//报错
```



方式二：调用String()函数。并将被转换的数据作为参数传递给函数。

说调用什么函数就直接写：例如调用string()函数，就写:String()

调用alert()函数，就写：alert()

对于String()函数，并将被转换的数据作为参数传递给函数

使用String（)函数做强制类型转换时

--对于Number和Boolean实际上就是调用toString()的方法

--但是对于null和undefined,就不会调用tostring()方法

它会将null直接转换为”null“

将undefined直接转换为”undefined"

//调用string()函数，来将a转换为字符串。

a=string(a);

#### 12.JS基础_强制类型转换-Number

将其他数据类型转换为Number

转换方式一：

使用Number()函数；

var a ="123";

//调用Number（）函数来将a转换为Number类型

a=Number(a);

console.log(typeof a);

console.log(a);

//执行返回：“number”  “123”



 var a ="abc";

//调用Number（）函数来将a转换为Number类型

a=Number(a);

console.log(typeof a);

console.log(a);

//执行返回：“number”  “NaN”



--字符串转数字

1.如果是纯数字的字符串，则直接将其转换为数字

2.如果字符串中有非数字的内容，则转换为NaN

3.如果空字符串是一个全身空格的字符串，则转换为0



//调用Number（）函数来将a转换为Number类型

a=Number(a);

a=true;

a=Number(a);

console.log(typeof a);

console.log(a);

//执行返回1，如果true改为false，执行则返回0





布尔转数字

true 转成1，false转成0；

null转成数字，--执行返回0,a=Number(a);

undefined 转换数字，NaN

a=null;

a=Number(a);

console.log(typeof a);

console.log(a);

//执行返回0





转换方式二：

这种方式专门来对付字符串转number

parseInt()把一个字符串转换为一个整数



//调用parseInt（）函数将a转换为Number

parseInt()可以将一个字符串中的有效的整数内容去处理

然后转换为Number

a=123a678pc

a=parseInt(a);

console.log(typeof a);

console.log(a);

执行返回  number  123



parseInt只会取整数



parseFloat（）作用和parseInt（）类似，不同的是他可以获得有效的小数，使用方法一样。只取从左到右的第一个小数点。



如果对非String使用parseInt()或parsefloat()

它会先将其转换为String然后操作

true  执行返回 Nan

#### 13.JS基础_其他进制的数字

十六进制，八进制，二进制在js中执行后，都是返回十进制的结果。

十六进制是以ox开头

八进制以07开头

二进制以0b开头

//像“070”这种字符串，有些浏览器会当成八进制解析，有些会当作十进制解析。

//可以在parseInt（）中传递一个第二个参数，来指定数字的进制

a="070";

a=parseInt(a,10);

#### 14.JS基07开头础_转换为Boolean

null和undefined转换成false

字符串转换为true

其他的数据类型转换为Boolean

使用boolean()函数

数字--布尔

除了0和NaN，其余的都是true

字符串--布尔

除了空串，其余的都是true

null和undefined都会转换为false

对象也会转换为true

#### 15.JS基础_算数运算符

运算符也叫操作符

通过运算符可以对一个或多个值进行运算,并获取运算结果

比如：typeof就是运算符，可以来获得一个值的类型

它会将该值的类型以字符串的形式返回

typeof 的返回值是字符串



var a=123;

var result =typeof a; 

console.log(result);

//执行返回number



算数运算符：加减乘除

当对非Number类型的值进行运算时，会将这些值转换为Number类型

任何值和NaN做运算都得NaN

如果对两个字符串进行加法运算，则会做拼串操作。

会将两个字符串拼接成一个字符串，并返回。



任何的值和字符串做加法运算，都会先转换为字符串。

然后再和字符串做了拼串的操作。



任何值和字符串相加都会转换为字符串，并做拼串操作

我们可以利用这一特点，来将一个任意的数据类型转换为String

我们只需为任意的数据类型+一个“”即可将其转换为String

这是一种隐式的类型转换，

由浏览器自动完成，实际上他也是调用String()函数



//任何值做-*/运算时都会自动转换为Number

我们可以利用这一特点做隐式的类型转换

可以通过为一个值-0*1/1来将其转换为Number

原理和Number()函数一样，使用起来更加简单。



%   取模运算，取余数。

result= 9%5;

console.log("result="+result);

//执行：“result=4"

#### 16.JS基础_一元运算符















#### 17.JS基础_自增和自减

自增++

通过自增可以使变量在自身的基础上增加1

对于一个变量自增以后，原变量的值会立即自增1

自增分成两种：后++（a++)和前++(++a)

无论是a++还是++a,都会立即使原变量的值自增1

不同的是a++和++a的值不同

a++的值等于原变量的值（自增前的值）

++a的值等于新值（自增后的值）



自增--

通过自减可以使变量在自身的基础上减一

自减分为两种，后--（a--)和前--（--a)

无论是a-- 还是--a 都会立即使原变量的值自减1

不同的是a-- 和--a的值不同

a--是变量的原值（自减前的值）

--a是变量的新值（自减以后的值）

```javascript
//20+22+22
var d =20;
var result=d++  +  ++d  + d;

```



#### 18.JS基础_自增练习

```javascript
var n1 =10;
var n2 =20;
var n =n1++;//n1=11   n1++=10

console.log('n='+n);  //10
console.log('n1='+n1);//11

n=++n1//n1=12   ++n1=12
console.log('n='+n);//12
console.log('n1='+n1);//12

n=n2--;//n2=19  n2--=20
console.log('n='+n);//20
console.log('n2='+n2);//19

n=--n2;//n2=18  ,--n2=18
console.log（'n='+n);//18
console.log('n2='+n2);//18

```



#### 19.JS基础_逻辑运算符
#### 20.JS基础_非布尔值的与或运算
#### 21.JS基础_赋值运算符
#### 22.JS基础_关系运算符
#### 23.JS基础_Unicode编码表
#### 25.JS基础_条件运算符
#### 26.JS基础_运算符的优先级
#### 27.JS基础_代码块
#### 28.JS基础_if语句（一）
#### 29.JS基础_if语句（二）
#### 30.JS基础_练习
#### 31.JS基础_if练习一
#### 32.JS基础_if练习二
#### 33.JS基础_条件分支语句
#### 34.JS基础_switch练习
#### 35.JS基础_while循环
#### 36.JS基础_while的练习
#### 37.JS基础_for循环
#### 38.JS基础_for循环
#### 39.JS基础_质数练习
#### 40.JS基础_补充质数练习
#### 41.JS基础_嵌套的for循环
#### 42.JS基础_练习
#### 43.JS基础_for循环练习
#### 44.JS基础_break和continue
#### 45.JS基础_质数练习的改进
#### 46.JS基础_对象的简介
#### 47.JS基础_对象的基本操作
#### 48.JS基础_属性名和属性值
#### 49.JS基础_基本数据类型和引用数据类型
#### 50.JS基础_对象字面量
#### 51.JS基础_函数的简介
#### 52.JS基础_函数的参数
#### 53.JS基础_函数的返回值
#### 54.JS基础_实参可以是任何值
#### 55.JS基础_返回值的类型
#### 56.JS基础_立即执行函数
#### 57.JS基础_方法
#### 58.JS基础_全局作用域
#### 59.JS基础_函数作用域
#### 60.JS基础_debug
#### 61.JS基础_this
#### 62.JS基础_this补充
#### 63.JS基础_使用工厂方法创建对象
#### 64.JS基础_构造函数
#### 65.JS基础_.构造函数修改
#### 66.JS基础_原型对象
#### 67.JS基础_原型对象
#### 68.JS基础_toString()
#### 69.JS基础_垃圾回收
#### 70.JS基础_数组简介
#### 71.JS基础_数组字面量
#### 72.JS基础_数组的四个方法
#### 73.JS基础_数组的遍历
#### 74.JS基础_数组练习
#### 75.JS基础_forEach
#### 76.JS基础_slice和splice
#### 77.JS基础_数组去重练习
#### 78.JS基础_数组的剩余方法
#### 79.JS基础_call和apply
#### 80.JS基础_arguments
#### 81.JS基础_Date对象
#### 82.JS基础_Math
#### 83.JS基础_包装类
#### 84.JS基础_字符串的方法
#### 85.JS基础_正则表达式的简介
#### 86.JS基础_正则语法
#### 87.JS基础_字符串和正则相关的方法
#### 88.JS基础_正则表达式语法
#### 89.JS基础_正则表达式语法
#### 90.JS基础_邮件的正则
#### 91.JS基础_DOM简介
#### 92.JS基础_事件的简介
#### 93.JS基础_文档的加载
#### 94.JS基础_dom查询
#### 95.JS基础_图片切换的练习
#### 96.JS基础_DOM查询
#### 97.JS基础_DOM查询
#### 98.JS基础_全选练习（一）
#### 99.JS基础_全选练习（二）
#### 100.JS基础_全选练习（三）
#### 101.JS基础_dom查询的剩余方法
#### 102.JS基础_dom增删改
#### 103.JS基础_添加删除记录-删除
#### 104.JS基础_添加删除记录-添加
#### 105.JS基础_添加删除记录-修改
#### 106.JS基础_a的索引问题
#### 107.JS基础_操作内联样式
#### 108.JS基础_获取元素的样式
#### 109.JS基础_getStyle()方法
#### 110.JS基础_其他样式相关的属性
#### 111.JS基础_事件对象
#### 112.JS基础_div跟随鼠标移动
#### 113.JS基础_事件的冒泡
#### 114.JS基础_事件的委派
#### 115.JS基础_事件的绑定
#### 116.JS基础_完成bind函数
#### 117.JS基础_事件的传播
#### 118.JS基础_拖拽（一）
#### 119.JS基础_拖拽（二）
#### 120.JS基础_拖拽（三）
#### 121.JS基础_滚轮的事件
#### 122.JS基础_键盘事件
#### 123.JS基础_键盘移动div
#### 124.JS基础_Navigator
#### 125.JS基础_History
#### 126.JS基础_Location
#### 127.JS基础_定时器简介
#### 128.JS基础_切换图片练习
#### 129.JS基础_修改div移动练习
#### 130.JS基础_延时调用
#### 131.JS基础_定时器的应用（一）
#### 132.JS基础_定时器的应用（二）
#### 133.JS基础_定时器的应用（三）
#### 134.JS基础_完成轮播图界面
#### 135.JS基础_完成点击按钮切换图片
#### 136.JS基础_完成轮播图
#### 137.JS基础_类的操作
#### 138.JS基础_二级菜单-完成基本功能
#### 139.JS基础_二级菜单-过渡效果
#### 140.JS基础_JSON