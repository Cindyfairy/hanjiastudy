# hanjiastudy
1-25-1study

思考题与习题

Python诞生和python之父：Python由荷兰数学和计算机科学研究学会的Guido van Rossum 于1990 年代初设计，作为一门叫做ABC语言的替代品。Python之父为吉多·范罗苏姆。

Python优点

A简单 – Python 是一种代表简单主义思想的语言。

B易学 – 就如同你即将看到的一样，Python 极其容易上手。前面已经提到了，Python 有极其简单的语法。

C免费、开源 – Python 是 FLOSS（自由/开放源码软件）之一。简单地说，你可以自由地发布这个软件的拷贝、阅读它的源代码、对它做改动、把它的一部分用于新的自由软件中。FLOSS 是基于一个团体分享知识的概念。

D高层语言 – 当你用 Python 语言编写程序的时候，你无需考虑诸如如何管理你的程序使用的内存一类的底层细节。

E可移植性 – 由于它的开源本质，Python 已经被移植在许多平台上（经过改动使它能够工作在不同平台上）。如果你小心地避免使用依赖于系统的特性，那么你的所有 Python 程序无需修改就可以在下述任何平台上面运行。这些平台包括 Linux、Windows、FreeBSD、Macintosh、Solaris、OS/2、Amiga、AROS、AS/400、BeOS、OS/390、z/OS、Palm OS、QNX、VMS、Psion、Acom RISC OS、VxWorks、PlayStation、Sharp Zaurus、Windows CE 甚至还有 PocketPC、Symbian 以及 Google 基于 Linux 开发的 Android 平台！

F解释性 – 这一点需要一些解释。一个用编译性语言比如 C 或 C++ 写的程序可以从源文件（即 C 或 C++ 语言）转换到一个你的计算机使用的语言（二进制代码，即0和1）。这个过程通过编译器和不同的标记、选项完成。当你运行你的程序的时候，连接/转载器软件把你的程序从硬盘复制到内存中并且运行。而 Python 语言写的程序不需要编译成二进制代码。你可以直接从源代码运行程序。在计算机内部，Python 解释器把源代码转换成称为字节码的中间形式，然后再把它翻译成计算机使用的机器语言并运行。

G面向对象 – Python 既支持面向过程的编程也支持面向对象的编程

H可扩展性 – 如果你需要你的一段关键代码运行得更快或者希望某些算法不公开，你可以把你的部分程序用 C 或 C++ 编写，然后在你的 Python 程序中使用它们。

I丰富的库 – Python 标准库确实很庞大

Python3相对于py2的改进：

1、python3 引入了 asyncio 来进行异步IO编成

2、print 在python2 是关键字，python3 是函数

3、编码问题，python3 不再有unicode对象， str 即为unicode

4、除法的变化。python 3 除法返回浮点数 5/2 = 2.5

5、类型注解（type hint）

6、优化的super() ,直接调用父类的方法

7、高级的解包操作， 如 a, b, *c= range(10)

8、限定关键字参数， 参数特别多的时候指定参数以防搞混

9、python3 重新跑出异常不会丢失栈信息

10、一切返回迭代器

11、新增yield from 链接生成器

12、新增内置库enum,mock, asyncio, ipaddress, concurrent, futures等

13、生成的pyc文件统一放到pycache

14、一些内置库修改。urllib，selector等

15、性能优化。

习题

1.怎样对python中的代码进行注释？

​ 1.单行注释：结尾后加"#"+注释

a = 3     #此处为注释
​ 2.多行注释：开头前和结尾后一行写下"""或'''

a = 2
"""
此处为注释
此处为注释
"""
a = 3
a = 2
'''
此处为注释
此处为注释
'''
a = 3
2.python有哪些运算符，这些运算符的优先级是怎样的？
运算符说明	Python运算符	优先级	结合性
小括号	( )	19	无
索引运算符	x[i] 或 x[i1: i2 [:i3]]	
属性访问	x.attribute	
乘方	**	
按位取反	~	
符号运算符	+（正号）、-（负号）
乘除	*、/、//、%	
加减	+、-
位移	>>、<<	
按位与	&
按位异或	^	
按位或	|	
比较运算符	==、!=、>、>=、<、<=
is 运算符	is、is not	
in 运算符	in、not in	
逻辑非	not
逻辑与	and	
逻辑或	or	
逗号运算符	exp1, exp2	
Ps:优先级数字越大的优先级越高

3.python 中 is, is not 与 ==, != 的区别是什么？
首先is，is not比较的是两个对象的id值是否相等，也就是比较俩对象是否为同一个实例对象，是否指向同一个内存地址，id(object)函数是返回对象object在其生命周期内位于内存中的地址，id函数的参数类型是一个对象。因此is和is not的参数类型也是对象，也就是比较俩对象是否为同一个实例对象，是否指向同一个内存地址。

而==和!=比较的是两个对象的内容是否相等

a = [4,5,6]
b = [4,5,6]
print(a == b)       #True
print(a is b)       #False
print(id(a))        #2375820246016
print(id(b))        #2375821562688
c = 3
d = 4
print(c == d)       #True
print(c is d)       #True
print(id(c))        #140718064346976
print(id(d))        #140718064346976
虽然每一次的id数值是不一样的，但可以发现c和d的id永远都是一样的，而a和b的永远不一样

4.python 中包含哪些数据类型？这些数据类型之间如何转换？
1.类型：

​ 数字类：

​ int整型、long长整型、float浮点数、complex复数

​ 布尔类：

​ bool布尔值

​ 字符串:

​ str类

​ 列表：

​ list

2.转换：

​ 1、list转str

​ 假设有一个名为test_list的list，转换后的str名为test_str

​ 则转换方法：

​ est_str = "".join(test_list)

​ 2、str转list

​ 假设有一个名为test_str的str，转换后的list名为test_list

​ 则转换方法：

​ test_list=list(test_str)

​ 3、对于一般的情况将 a 转成目标类型

​ 如转int整型 int(a)其他情况类似
1-25-2位运算
练习题：

leetcode 习题 136. 只出现一次的数字

给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元素。

尝试使用位运算解决此题。

我还没学到python后面的语法，不知道怎么写。但是可以写写思路。

这题应当运用异或运算中，A^A=0，A^0=A。

遍历数组，每有两个相同的元素就都置0，于是剩下最后一个不是0的元素，就是要找的只出现了一次的元素。


