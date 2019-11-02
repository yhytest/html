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

js中为我们提供了三种逻辑运算符

！非   ！可以用来对一个值进行非运算

true变false,false变true

如果不对一个值进行两次取反，他的值不会变化。

如果对非布尔值进行运算，则会将其转换为布尔值，然后再取反。

所以我们可以利用该特点，来将一个其他的数据类型转换成布尔值

可以为一个任意数据类型取两次反，来将其转换为布尔值。

var a =true;

a=!a;

console.log（“a="+a);

//执行返回a=false;



&&与

可以对符号两边的值进行与运算并返回结果

运算规则

如果两个值都是true则返回true

var result =true&&true;

只要有一个false，就返回false

result=true&&false;

result=false&&true;

result=false&&false;

//第一个值为true,会检查第二个值

true&&alert("看我出不出来"）;   会执行出弹框

//第一个值为false,不会检查第二个值

false&&alert("看我出不出来");   不会执行出弹框



||或   ||可以对符号两边的值进行或运算并返回结果



两个都是false，则返回false

result=false||false;

只有一个true,就返回true

result=true||true;

result=false||true;

result=true||true;



JS中的”或“属于短路的或

如果第一个值为true,则返回true,不会检查第二个值

如果第二个值为false,则会检查第二个值

#### 20.JS基础_非布尔值的与或运算

//true&&true

与运算，如果两个值都为true,则返回后边的

var result =2&&1;

console.log("result= "result);

//执行：”result=1";



false&&true

result=0&&2;

result=2&&0;

result=NaN&&0;

//是false，执行得false值，是NaN得NaN

//与运算中，如果两个值中有false，则返回靠前的false

result=NaN&&0;执行返回NaN,

result=0&&NaN;执行返回0;



与运算：

如果第一个值为true,则直接返回第二个值。

如果第一个值为false,则直接返回第一个值。





或运算：

true||true

如果第一个值为true,则直接返回第一个值。

result=2||1;

result=2||NaN；

result=2||0;

如果第一个值为false,则直接返回第二个值

result=NaN||1;

result=NaN||0;

#### 21.JS基础_赋值运算符

=：

可以将符号右侧的值赋值给符号左侧的变量

+=：

a+=5;===a=a+5;

-=:

a-=5;===a=a-5;

a*=5;

a*=5;==a=a*5;

/=;

a/=5;===a=a/5;

%=;

a%=5;===a=a%5;

#### 22.JS基础_关系运算符\

大于

小于

大于等于

小于等于

非布尔值的比较

```javascript
console.log("result=" +result);
console.log(1>true);//false
console.log(1>=true);//true
console.log(1>"0");//true
console.log(10>null);//true
console.log(10>"hello"）;//true
console.log(10<"hello"）;//false  hello转成数字是nan
            //任何值和Nan做任何比较都是false
 console.log("1"<"5");//true
//如果符号两侧的值都是字符串时，不会将其转换为数字进行比较
//而会分别比较字符串中字符的Unicode编码
```

#### 23.JS基础_Unicode编码表

js中在字符串中使用转义字符\u

html在字符串中使用转义字符要十六进制转换成十进制&#编码



#### 24.JS基础_相等运算符

相等运算符用来比较两个值是否相等

如果相等会返回true，否则则返回false

使用==来做相等运算

var a =10;

console.log(a==4);//false

console.log("1"==1);//true

当使用==来比较两个值时，如果值的类型不同，则会自动进行类型转换，将其转换为

相同的类型，然后再比较

console.log("1"==1);  //true

console.log("true"=="1");//true

console.log(true =="hello");//false

console.log(null==0);//false   



undefined衍生自null

所以这两个值做相等判断是否，会返回true

console.log(undefined ==null); //true



NaN不和任何值相等，包括它本身

console.log(NaN==NaN);//false



var b=NaN;

判断B的值是否是NaN

console.log(b==NaN);

可以通过ISnan()函数来判断一个是否是NaN,

如果该值是NaN则返回true，否则则返回false

console,log(isNaN(b));//true

var b =123,则上面返回false



不相等 用来判断两个值是否不相等，如果不相等则返回true,否则返回false

console.log(10!=5);//true

console.log(10!=10);//false

console.log("abcd"!="abcd");//false

console.log("1"!=1);//false

使用！=不相等做运算

不相等也会对变量进行自动的类型转换，如果转换后相等它也会返回false





====全等   用来判断两个字是否全等，它和相等类似。不同的是不会做自动的类型转换。

如果两个值的类型不同，自动返回false、

console.log("123==123");//true

console.log("123===123");/false  类型不同自动返回false



console.log(null==undefined);//true

console.log(null===undefined);//false



!==  不全等  用来判断两个值是否不全等，和不等类似，不同的是它不会做自动的类型转换

如果两个值的类型不同，直接返回true

console.log(1!=1);//true



#### 25.JS基础_条件运算符

#### 26.JS基础_运算符的优先级
#### 27.JS基础_代码块
#### 28.JS基础_if语句（一）
#### 29.JS基础_if语句（二）
#### 30.JS基础_练习
#### 31.JS基础_if练习一

```javascript
var score =prompt("请输入小明的期末成绩（0-100）：")；
//判断值是否合法
if (score >100 || score<0 || isNaN(SCORE)){
    alert("拉出去毙了~~")；
}else{
    if(score==100){
        //奖励一台宝马
        alert("宝马，拿去~~~")；
    }else if(score>=80){
        //奖励一个手机
        alert("手机，拿去玩~~")；
     }else if（score>=60){
         alert("参考书，拿去看~~")；
        }else{
            alert("棍子一根~~")
        }
}
```



#### 32.JS基础_if练习二

//高：180cm,富：1000万以上，帅500以上

如果这三个条件都满足，则“我一定要嫁给他”

如果三个条件有为真的情况，则“嫁吧，比上不足，比下有余。”

如果三个条件都不满足。则“不嫁”

```javascript
var height =prompt("请输入您的身高（cm);");
var money =prompt("请输入您的财务（w);");
var face =prompt("请输入您的颜值（px):");
//如果这三个条件同时满足，则，我一定要嫁给他
if(height>188&&money>1000&&face>500){
    alert("我一定要嫁给他~~")；
}else if(height>180||money>1000!!face>500){
    //如果三个条件有为真的情况，则，嫁吧，比上不足，比下有余
    alert（“嫁吧，比上不足，比下有余”）；
}else{
    //如果三个条件都不满足。则“不嫁”
    alert("不嫁")；
}

```



#### 33.JS基础_条件分支语句

```javascript


```

#### 34.Js基础_switch练习

```
var score =88;
switch(parseInt(score/10)){
        case 10;
        case 9;
        case 8;
        case 7;
        case 6;
        console.log("合格")；
        break；
        defalt;
        console.log("不合格")；
        break;
   
}

```

#### 35.JS基础_while循环

while语句在执行时，先对条件表达式进行求值判断，如果值为true,则执行循环体，

循环体执行完毕以后，继续对表达式进行判断

如果为true,则继续执行循环体，以此类推

如果值为false,则终止循环体。

var n=1;

向这种将条件表达式写死为true的循环，叫做死循环。

该循环不会停止，除非浏览器关闭，死循环在开发中慎用。

可以使用break,来终止循环。

while(true){

alert(n++);

//退出循环

break;

//判断n是否是10

if(n==10){

break;

}

}

//创建一个循环，往往需要三个步骤

1.创建初始化一个变量

2.在循环中设置一个条件表达式

3.定义一个更新表达式，每次更新初始化变量





do...while

语法：

do{

语句。。。

}while(条件表达式)

先执行后判断。先执行do.里面的

do。。。while可以保证循环体至少执行一次，而while不能



实际上两个语句功能类似，不同的是while是先判断后执行。

而do...while是先执行do里面的语句，先执行，后判断。第一次执行不管您条件成不成立。

#### 36.JS基础_while的练习

```javascript

			/*
			 * 假如投资的年利率为5%，试求从1000块增长到5000块，需要花费多少年
			 * 
			 * 1000 1000*1.05
			 * 1050 1050*1.05
			 */
			
			//定义一个变量，表示当前的钱数
			var money = 1000;
			
			//定义一个计数器
			var count = 0;
			
			//定义一个while循环来计算每年的钱数
			while(money < 5000){
				money *= 1.05;
				
				//使count自增
				count++;
			}
			
			
			//console.log(money);
			console.log("一共需要"+count+"年");


/*
			 * 	从键盘输入小明的期末成绩:
			 *	当成绩为100时，'奖励一辆BMW'
			 *	当成绩为[80-99]时，'奖励一台iphone15s'
			 *	当成绩为[60-80]时，'奖励一本参考书'
			 *	其他时，什么奖励也没有
			 */
			
			/*
			 * prompt()可以弹出一个提示框，该提示框中会带有一个文本框，
			 * 	用户可以在文本框中输入一段内容，该函数需要一个字符串作为参数，
			 * 	该字符串将会作为提示框的提示文字
			 * 
			 * 用户输入的内容将会作为函数的返回值返回，可以定义一个变量来接收该内容
			 */
			//将prompt放入到一个循环中
			while(true){
				//score就是小明的期末成绩
				var score = prompt("请输入小明的期末成绩(0-100):");
				//判断用户输入的值是否合法
				if(score >= 0 && score <= 100){
					//满足该条件则证明用户的输入合法，退出循环
					break;
				}
				
				alert("请输入有效的分数！！！");
			}
			
			
			
			//判断值是否合法
			if(score > 100 || score < 0 || isNaN(score)){
				alert("拉出去毙了~~~");
			}else{
				//根据score的值来决定给小明什么奖励
				if(score == 100){
					//奖励一台宝马
					alert("宝马，拿去~~~");
				}else if(score >= 80){
					//奖励一个手机
					alert("手机，拿去玩~~~");
				}else if(score >= 60){
					//奖励一本参考书
					alert("参考书，拿去看~~~");
				}else{
					alert("棍子一根~~");
				}
			}
			
```



#### 37.JS基础_for循环

```javascript
/*
			 * for语句，也是一个循环语句，也称为for循环
			 * 	在for循环中，为我们提供了专门的位置用来放三个表达式：
			 * 		1.初始化表达式
			 * 		2.条件表达式
			 * 		3.更新表达式
			 * 
			 *  for循环的语法：
			 * 		for(①初始化表达式;②条件表达式;④更新表达式){
			 * 			③语句...
			 * 		}
			 * 
			 * 		for循环的执行流程：
			 * 			①执行初始化表达式，初始化变量（初始化表达式只会执行一次）
			 * 			②执行条件表达式，判断是否执行循环。
			 * 				如果为true，则执行循环③
			 * 				如果为false，终止循环
			 * 			④执行更新表达式，更新表达式执行完毕继续重复②
			 */
			
			//创建一个执行10次的while循环
			//初始化表达式
			/*var i = 0;
			
			//创建一个循环，定义条件表达式
			while(i < 10){
				//设置更新表达式
				alert(i++);
			}*/
			
			for(var i = 0 ; i < 10 ; i++ ){
				alert(i);
			}
			
			/*
			 * for循环中的三个部分都可以省略，也可以写在外部
			 * 	如果在for循环中不写任何的表达式，只写两个;
			 * 	此时循环是一个死循环会一直执行下去，慎用
			 * 	for(;;){
					alert("hello");
				}
			 */


/*
			 * 打印1-100之间所有奇数之和
			 */
			
			//创建一个变量，用来保存奇数之和
			//var sum = 0;
			
			//打印1-100之间的数
			for(var i=1 , sum=0 ; i<=100 ; i++){
				
				//判断i是否是奇数
				//不能被2整除的数就是奇数
				if(i%2 != 0){
					//如果i除以2有余数则证明i是奇数
					//console.log(i);
					sum = sum+i;
				}
			}
			
			console.log("奇数之和为 : "+sum);
```



#### 38.JS基础_for循环

```javascript
/*
			 * 打印1-100之间所有7的倍数的个数及总和
			 */
			//定义一个变量，来保存总和
			var sum = 0;
			//定义一个计数器，来记录数量
			var count = 0;
			
			//打印1-100之间所有的数
			for(var i=1 ; i<=100 ; i++){
				
				//判断i是否是7的倍数
				if(i % 7 == 0){
					//console.log(i);
					sum += i;
					//使计数器自增1
					count++;
					
				}
				
			}
			
			//输出总和
			console.log("总和为:"+sum);
			//输出总数
			console.log("总数量为:"+count);
```



#### 39.JS基础_质数练习

```javascript
	/*
			 * 打印出1-100之间所有的质数
			 */
			
			//打印2-100之间所有的数
			for(var i=2 ; i<=100 ; i++){
				
				//创建一个布尔值，用来保存结果，默认i是质数
				var flag = true;
				
				//判断i是否是质数
				//获取到2-i之间的所有的数
				for(var j=2 ; j<i ; j++){
					
					//判断i是否能被j整除
					if(i%j == 0){
						//如果进入判断则证明i不是质数,修改flag值为false
						flag = false;
						
					}
					
				}
				
				//如果是质数，则打印i的值
				if(flag){
					console.log(i);
				}
				
			}
```



#### 40.JS基础_补充质数练习

```javascript
	
			//测试如下的程序的性能
			//在程序执行前，开启计时器
			//console.time("计时器的名字")可以用来开启一个计时器
			//它需要一个字符串作为参数，这个字符串将会作为计时器的标识
			console.time("test");
			
			//打印2-100之间所有的数
			for(var i=2 ; i<=100000 ; i++){
				var flag = true;
				for(var j=2 ; j<=Math.sqrt(i) ; j++){
					if(i%j == 0){
						//如果进入判断则证明i不是质数,修改flag值为false
						flag = false;
						//一旦进入判断，则证明i不可能是质数了，此时循环再执行已经没有任何意义了
						//使用break来结束循环
						break;
						
						//不加break 215ms
						//加break 25ms
						//修改j<=后 2.6
					}
				}
				//如果是质数，则打印i的值
				if(flag){
					//console.log(i);
				}
			}
			
			//终止计时器
			//console.timeEnd()用来停止一个计时器，需要一个计时器的名字作为参数
			console.timeEnd("test");
			
			/*
			 * 36
			 * 1 36
			 * 2 18
			 * 3 12
			 * 4 9
			 * 6 6
			 */
			
			//可以通过Math.sqrt()对一个数进行开方
			//var result = Math.sqrt(97);
			
			//console.log("result = "+result)
			
```



#### 41.JS基础_嵌套的for循环

```javascript
	/*
			 
			 	通过程序，在页面中输出如下的图形：
			 	
			 	*      1   <1   i=0
			 	**     2   <2   i=1
			 	***    3   <3   i=2
			 	****   4   <4   i=3
			 	*****  5   <5   i=4
			 	
			 	*****
			 	*****
			 	*****
			 	*****
			 	*****
			 	
			 	***** 1   j<5(5-0)  i=0
			 	****  2	  j<4(5-1)  i=1
			 	***   3   j<3(5-2)  i=2
			 	**    4   j<2(5-3)  i=3
			 	*     5   j<1(5-4)  i=4
			 	
			 
			 */
			
			//向body中输出一个内容
			//document.write("*****<br />");
			
			//通过一个for循环来输出图形
			//这个for循环执行几次，图形的高度就是多少
			//它可以用来控制图形的高度
			for(var i=0 ; i<5 ; i++){
				
				/*
				 * 在循环的内部再创建一个循环，用来控制图形的宽度
				 * 目前我们的外部的for循环执行1次，内部的就会执行5次
				 * 内层循环可以来决定图形的宽度，执行几次图形的宽度就是多少
				 */
				/*for(var j=0 ; j<i+1 ; j++){
					document.write("*&nbsp;&nbsp;&nbsp;");
				}*/
				for(var j=0 ; j<5-i ; j++){
					document.write("*&nbsp;&nbsp;&nbsp;");
				}
				
				//输出一个换行
				document.write("<br />");
				
				
			}
			
```



#### 42.JS基础_练习

```javascript
/*
			 * 1.打印99乘法表
			 * 	 1*1=1
			 * 	 1*2=2 2*2=4
			 * 	 1*3=3 2*3=6 3*3=9
			 * 	 1*4=4 2*4=8 3*4=12 4*4=16	
			 * 						....9*9=81
			 * 
			 * 2.打印出1-100之间所有的质数
			 */
			
			//创建外层循环，用来控制乘法表的高度
			for(var i=1 ; i<=9 ; i++ ){
				//创建一个内层循环来控制图形的宽度
				for(var j=1 ; j<=i ; j++){
					document.write("<span>"+j+"*"+i+"="+i*j+"</span>");
				}
				
				//输出一个换行
				document.write("<br />");
				
			}
			
			
		</script>
		<style type="text/css">
		
			body{
				width: 2000px;
			}
			
			span{
				display: inline-block;
				width: 80px;
			}
```



#### 43.JS基础_for循环练习
#### 44.JS基础_break和continue

```javascript
//break 关键字可以用来退出switch或循环语句
//不能在if语句中使用break和continue
//break关键字，会立即终止离他最近的那个循环语句

/*for(var i=0;i<5;i++){
    console.log(i);
    if(i ==2);{
        break;
    }
}
*/

可以为循环语句创建一个label,来标识当前的循环
label:循环语句
使用break语句时，可以在break后跟着一个label,
   这样break将会结束指定的循环，而不是最近的。
outer
for(var i=0;i<5;i++){
    console.log("@外层循环“+i)
                for(var j=0;j<5;j++){
        break outer;
        console.log("内存循环：”+j);
                    
    }
}
    
    continue关键字可以用来跳过当次循环
    同样continue也是默认只会对离他最近的循环循环起作用
    for(var i=0;i<5;i++){
        if(i==2){
            continue;
        }
        console.log(i);
    }
    
    outer;
    
    for(var i=0;i<5;i++){
        for(var j=0;j<5;j++){
            continue;
        
        console.log("-->"+j);
       
    }
    console.log("@--->"+i);
    }
    

```



#### 45.JS基础_质数练习的改进

```
			
			//测试如下的程序的性能
			//在程序执行前，开启计时器
			//console.time("计时器的名字")可以用来开启一个计时器
			//它需要一个字符串作为参数，这个字符串将会作为计时器的标识
			console.time("test");
			
			//打印2-100之间所有的数
			for(var i=2 ; i<=100000 ; i++){
				var flag = true;
				for(var j=2 ; j<=Math.sqrt(i) ; j++){
					if(i%j == 0){
						//如果进入判断则证明i不是质数,修改flag值为false
						flag = false;
						//一旦进入判断，则证明i不可能是质数了，此时循环再执行已经没有任何意义了
						//使用break来结束循环
						break;
						
						//不加break 215ms
						//加break 25ms
						//修改j<=后 2.6
					}
				}
				//如果是质数，则打印i的值
				if(flag){
					//console.log(i);
				}
			}
			
			//终止计时器
			//console.timeEnd()用来停止一个计时器，需要一个计时器的名字作为参数
			console.timeEnd("test");
			
			/*
			 * 36
			 * 1 36
			 * 2 18
			 * 3 12
			 * 4 9
			 * 6 6
			 */
			
			//可以通过Math.sqrt()对一个数进行开方
			//var result = Math.sqrt(97);
			
			//console.log("result = "+result)
```



#### 46.JS基础_对象的简介

```javascript
/*
*js中数据类型
-string字符串
-Number数值
-Boolean布尔值
-Null控制
-Undefined未定义
-以上这五种类型属于数据类型，以后我们看到的值只要不是上边的5种，全都是对象
-object 对象
基本数据类型都是单一的值“hello"123 true,
值和值之间没有任何的联系
在js中表示一个人的信息（name  gender  age);
var name="孙悟空";
var gender="男";
var age =18;
如果使用基本数据类型的数据，我们所创建的变量都是独立，不能成为一个整体。
对象属于一种复合的数据类型，在对象中可以保存多个不同数据类型的属性。

对象的分类：
1.内建对象
-由ES标准中定义的对象，在任何的ES的实现中都可以使用
-比如，Math String Number Boolean Function Object...

2.宿主对象
由JS的运行环境提供的对象，目前来讲主要指由浏览器提供的对象
-比如BOM  DOM

3.自定义对象
-由开发人员自己创建的对象


创建的对象
使用new关键字调用的函数，是构造函数CONSTRUCTOR  constructor
构造函数是专门用来创建对象的函数
使用typeof 检查一个对象时，会返回object

var obj =new object();


/*
*在对象中保存的值称为为属性
向对象添加属性
语法：对象.属性名=属性值；

向obj中添加一个name属性
obj.name="孙悟空"；
向obj中添加一个gender属性
obj.gender="男"；
向obj中添加一个age属性
obj.age=18;

"读取对象中的属性"
”语法：对象.属性名“
如果读取对象中没有的属性，不会报错而是会返回undefined

console.log(obj.gender);
console.log(obj.hello);

修改对象的属性值
语法：对象,属性名=新值

obj.name="tom";
删除对象的属性
语法：delete 对象.属性名

delete obj.name;
console.log(obj.age);

```



#### 47.JS基础_对象的基本操作
#### 48.JS基础_属性名和属性值

```javascript
//向对象中添加属性
属性名：
-对象的属性名不强制要求遵守标识符的规范
声明乱七八糟的名字都可以使用
但是我们使用是还是尽量按照标识符的规范去做

obj.name="孙悟空"；
obj.var=”hello";

如果要使用特殊的属性名，不能采用.的方式来操作
需要使用另一种方式
语法：对象【”属性名“】=属性值
读取时也需要采用这种方式

使用【】这种形式去操作属性，更加的灵活
在【】中可以直接传递一个变量，这样变量值是多少就会读取那个属性

obj["123"]=789;
obj["nihao"]="你好"；
var n="nihao";
//console.log(obj["123"]);

/属性值
js对象的属性值，可以是任意的数据类型
甚至也可以是一个对象

obj.test=true;
obj.test=null
obj.test=undefined;

//创建一个对象
var obj2=new object();
obj2.name="猪八戒"；

//将obj2设置为obj的属性
obj.test=obj2;

//console.log(obj.test.name);
in 运算符
通过该运算符可以检查一个对象中是否含有指定的属性
如果有则返回true,没有则返回false
语法
”属性名“in 对象
console.log(obj.test2);
检查obj中是否含有台test2属性
console.log("test2"in obj);
console.log("test" in obj);
console.log("name"in obj)
```



#### 49.JS基础_基本数据类型和引用数据类型

基本数据类型：striing,Number,Boolean,Null,Undefined

引用数据类型 Object

JS中的变量都是保存到栈内存中的，基本数据类型的值自减在栈内存中存储，值与值之间是独立存在，修改一个变量不会影响其他的变量

对象是保存在堆内存中的，每创建一个新的对象，就会在堆内存中开辟出一个新的空间

而变量保存的是对象的内存地址（对象的引用 ），如果两个变量保存的是同一个对象引用，当一个通过变量修改属性时，另一个也会受到影响



var a=123;

var b=a;

a++;

/*console.log(“a=”+a);

console.log("b="+b);

*/

var obj =new object();

obj.name="孙悟空"；

var obj2=obj;

//修改obj的name属性

obj.name="猪八戒"；

/*console.log(obj.name);

console.log(obj2.name);*/



设置obj2为null

obj2=null;

/*console.log(obj);

console.log(obj2);*/

var c=10;

var d=10;

//console.log(c==d);

var obj3=new Object();

var obj4=new Object();

obj3.name="沙和尚"；

obj4.name=”沙和尚“；



/*console.log(obj3);

console.log(obj4);

/*当比较两个基本数据类型的值时，就是比较值。

而比较两个引用数据类型时，它是比较的对象的内存地址

如果两个对象是一模一样的，但是地址不同，它也是会返回false.*/



console.log(obj3==obj4);

#### 50.JS基础_对象字面量

//创建一个对象

var obj =new Object();

//使用对象字面量来创建一个对象

var obj={};

//console.log(typeof obj);

obj.name="孙悟空"；

//console.log(obj.name);

使用对象字面量，可以在创建对象时，直接指定对象中的属性

语法：{属性名：属性值，属性名：属性值。。。}

对象字面量的属性名可以加引号也可以不加，建议不加

如果要使用一些特殊的名字，则必须加引号

属性名和属性值是一组一组的名值对结构，

名和值自减使用：连接，多个名值对之间使用，隔开

如果一个属性之后没有其他的属性了，就不要写



var obj2={

name:"猪八戒"，

age:13,

gender:"男"；

test:{name:"沙僧"}

}；

console.log(obj2.test);

#### 51.JS基础_函数的简介

函数function

函数也是一个对象

函数中可以封装一些功能（代码），在需要时可以执行这些功能（代码）

函数中可以保存一些代码在需要的时候调用

使用typeof检查一个函数对象时，会返回function

我们在实际开发中很少使用构造函数来创建一耳光函数对象

创建一个函数对象，可以将要封装的代码以字符串的形式传递给构造函数

var fun=new function("console.log('hello这是我的第一个函数’）；”)；

封装到函数中的代码不会立即执行

函数中的代码会在函数调用的时候执行

调用函数 语法：函数对象（）

当调用函数时，函数中封装的代码会按照顺序执行

fun();

使用函数声明 来创建一个函数

语法：

function 函数名（【形参1，形参2。。。形参N】）{

语句。。。}

function fun2(){

console.log("这是我的第二个函数~~~")；

alert("哈哈哈哈")；

document.write("~~~kaixin~~~");

}

//console.log(fun2);

调用fun2

fun2();



使用函数表达式来创建一个函数

var 函数名=function（【形参1，形参2。。。形参N】）{

语句。。。}



var fun3 =function(){

console.log("我是匿名函数中的封装的代码")

}；

fun3();

#### 52.JS基础_函数的参数

定义一个用来求两个数和的函数

可以在函数的（）中来指定一个或多个形参（形式参数）

多个形参之间使用，隔开，声明形参就相当于在函数内部声明了对应的变量

但是并不赋值

function sum(a,b){

console.log("a ="+a);

console.log("b="+b);

console.log(a+b);

}



在调用函数时，可以在（）中指定实参（实际参数）

实参将会赋值给函数中对应的形参

sum（1,2）；

sum（123,456）；

调用函数时解析器不会检查实参的类型

所以要注意，是否有可能会接受到非法的参数，如果有可能则需要对参数进行类型的检查

函数的实参可以是任意的数据类型

sum(123,"hello");

sum(true,false);

调用函数时，解析器也不会检查实参的数量

多余实参不会被赋值

如果实参的数量少于形参的数量，则没有对一你个实参的形参将是undefined

sum(123,455,"hello",true,null);

sum(123);

#### 53.JS基础_函数的返回值

创建一个函数，用来计算三个数的和，可以使用reture来设置函数的返回值

语法：reture值

reture后的值将会作为函数的执行结果返回

可以定一个一个变量，来接受该结果

在函数中reture后的语句都不会执行

如果reture语句后不跟任何值就相当于返回一个undefined，

如果函数中不写return,则也会返回undefined

return后可以跟任意类型的值



function sum(a,b,c){

//alert(a+b+c);

var d=a+b+c;

return d ;

//return  undefined

}

调用函数

变量result的值就是函数的执行结果

函数返回声明result的值就是什么

var result =sum(4,7,8);

//var result=alert("hello");

console.log("result="+result);

#### 54.JS基础_实参可以是任何值

定义一个函数，判断一个数字是否是偶数，如果是返回true,否则返回false

function isou(num){

return num%2==0l

}

var result=isou(15);

//console.log("result="result);



定义一个上述，可以根据半径计算一个圆的面积，并返回计算结果

3.148*r*r

function mianji(r){

return3.14rr

}

result=mianji(5);

//console.log("result="+result);

//创建一个函数，可以在控制台中输出一个人的信息

可以输出人的name,age,gender,address

实参可以是任意的数据类型，也可以是一个对象

当我们的参数过多时，可以将参数封装到一个对象中，然后通过对象传递

function sayhello（o){

}



//console.log("o="+o);

console.log("我是"+o.name+",今年我“+o.age+"岁了，”+“我是一个”+o.gender+"人"+“，我住在”+o.address);

}

//sayhello("猪八戒"，28,"高老庄"，“男”)；

//创建一个对象

var obj={

name:="孙悟空"，

age:18,

address:"花果山"，

gender:"男"

}；

//sayhello(obj);

实参可以是一个对象，也可以说一个函数

function fun(a){

console.log("a="+a);

//a(obj)

//fun(sayhello);

//fun(function(){alert("hello")});

fun(mianji(10)；)

}

//mianji()

调用函数

相当于使用的函数的返回值

//mianji

函数对象

相当于自己使用函数对象

#### 55.JS基础_返回值的类型

function fun(){

alert("函数要执行力~~~")}；

for(var i=0;i<5;i++){

if(i==2){

//使用break可以退出当前的循环

//break;

//continue用于跳过当次循环

//continue;

//使用returen可以结束整个函数

//return;

}

console.log(i);

}

alert("函数执行完了~~~")；

}

//fun();

//返回值可以是任意的数据类型

也可以是一个对象，也可以是一个函数

function fun2(){

//返回一个对象

return(name:"沙和尚")；

}

var a=fun2();

//console.log("a="+a);

function fun3(){

//在函数内部再声明一个函数

function fun4(){

alert("我是fun4");

}

//将fun4函数对象作为返回值返回

return fun4；

}

a=fun3();

//console.log(a);

//a();

fun3()();

#### 56.JS基础_立即执行函数

//函数对象（）

立即执行函数

函数定义完，立即被调用，这种函数叫做立即执行函数

立即执行函数往往只会执行一次

（function(){

alert("我是一个匿名的函数！！！")；

}）（）;*/

(function(a,b){

console.log("a="+a);

console.log("b="+b);

})(123,456);

#### 57.JS基础_方法

创建一个对象

var obj=new object();

向对象中添加属性

obj.name="孙悟空"；

obj.age=18;

对象的属性值可以是任何的数据类型，也可以是个函数

obj.sayName=function(){

console.log(obj.name);

};

function fun(){

console.log(obj.name);

}

//console.log(obj.sayName);

//调方法

obj.sayName();

//调函数

//fun();

函数也可以成为对象的属性

如果一个函数作为一个对象的属性保存

那么我们称这个函数时这个对象的方法

调用这个和函数就说调用对象的方法（method)

但是它只是名称上的区别没有其他的区别

var obj2={

name：“猪八戒”，

age:18

sayName:function(){

console.log(obj2.name);

}

};

boj2.sayName();

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