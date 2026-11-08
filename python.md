# python

### python的彩蛋

```python
import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

### 小游戏

```python
"""用python设计第一个游戏"""
temp=input("请输入一个数")
guess=int(temp)
if guess==8:
    print("you are right")
else:
    print("no,you are wrong")

```

| 符号   | 说明                     |
| ------ | ------------------------ |
| \\\    | 反斜杠                   |
| \\'    | 单引号                   |
| \\a    | 响铃                     |
| \\b    | 退格符                   |
| \\n    | 换行符                   |
| \\t    | 水平制表符（table）      |
| \\v    | 垂直制表符（VT）         |
| \\r    | 回车符（CR）             |
| \\f    | 换页符（FF）             |
| \\ooo  | ooo为八进制              |
| \\xhh  | hh为十六进制             |
| is     | 判断两个数的id是否相等   |
| is not | 判断两个数的id是否不相等 |

python的缩进非常重要
可以直接print(x),不用像c语言要加引号
变量名：字母、数字、下划线组成，不能以数字开头
print(x,y)		--->x y(中间的逗号不见了)

> x,y=y,x		意思是交换x,y的值
> alt+p是上一句

单双引号都能表示字符串，如果需要打印let's可以用双引号，也可以用转意字符\
如果想表示路径如：C:\Users\31161\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Python 3.15
那么就得在\前面再加上\
也可以在print（r“    ”）第一个引号前加上r
字符串可以相加，就是文本的拼接
也可以用字符串*1000，表示1000遍字符串

>a=3
>while a>0:
>	print("hello")
>	break

在python中需要注意缩进，语句的结尾不是都要使用标点符

```python

count=3
while count>0:
    temp=input("请输入一个数")
    guess=int(temp)
    if guess==8:
        print("you are right")
        break
    else:
        if guess>8:
            print("这个数大了")
        else:
            print("这个数小了")
    count=count-1
print("游戏结束")

```

### 随机数

```python
import random
random.randint(a,b)
```

a,b表示随机数的范围

### 精准化浮点数

浮点数在计算机中的储存不是10进制，所以会出现误差
decimal就是10进制的意思

```python
import decimal
a=decimal.Decimal('0.1')
```

e-5,表示10的-5次方

### 复数

x=1+2j
x.real		x的实部
x.imag		x的虚部

| x//y           | 地板除(先做除法，结果是不是整数，那么输出比这个整数小的整数)<br />-1.2是-2 |
| -------------- | ------------------------------------------------------------ |
| abs(s)         | 绝对值                                                       |
| complex(re,im) | 返回一个复数re是实部，im是虚部                               |
| c.comjugate    | 返回c的共轭函数                                              |
| pow(x,y)       | 计算x的y次方                                                 |
| divmod(x,y)    | 返回（x//y，x%y）                                            |
| x**y           | x的y次方                                                     |

abs(z)		z是一个复数
返回复数的模
把浮点数转为int，是直接将小数部分去掉，不是四舍五入

如果pow(a,b,c)		（a的b次方）与c的余数

> import fractions
>
> f1 = fractions.Fraction(1, 3)
> 这个函数会自动约分

### 布尔类型

bool(a)		判断a是真是假
False有：

1. none,False
2. 0,0.0,0j,Decimal(0),Fraction(0,1)
3. 空的序列和集合：‘’，（），[],{},set(),range(0)

| and  | 两边都为ture，则为ture                          |
| ---- | ----------------------------------------------- |
| or   | 左右两边只要有一个ture，就是ture                |
| not  | 如果是ture,变为false<br />如果是false，变为ture |

### 短路逻辑

从左往右，只有当第一个数无法确认逻辑运算的结果时，才对第二个数进行判断，输出决定结果的那个值

### 优先级(从低到高)

| lambda  | Lambda表达式   |
| ------- | -------------- |
| if else | 条件表达式     |
| or      | 或             |
| and     | 与             |
| not     | 非             |
| <,>     | 各种比较运算符 |
| \|      | 按位或         |
| ^       | 按位异或       |
| &       | 按位与         |
| <<,>>   | 移位           |

### 分支与循环

通过缩进来表示代码关系

判断多个条件（在某个条件满足就会结束，不会重复进行无意义的条件判断）

```python
if condition1:
    statement(s)
elif condition2:
    statement(s)
elif condition3:
    statement(s)
```

```python
if condition1:
    statement(s)
elif condition2:
    statement(s)
elif condition3:
    statement(s)
else:
    print("前面的条件都不满足")
```

条件表达式

> 条件成立时执行的语句 if condition else 条件不成立时执行的语句

```python
age=input("请输入你的年龄：")
a=int(age)
print("未成年禁止入内") if a<17 else print("欢迎光临")
```

当字符串和变量想拼接在一起打印时，需要用==，==分割字符串和变量

> max=a if a>b else b

用了条件表达式就不用在else后面再赋值了

比较两个数的大小

```python
a=int(input("请输入一个数："))
b=int(input("请输入一个数："))
max=a if a>b else b
print("max是",max)
```

i+=1		就是i=i+1

### contibue

直接跳到前面，后面的语句不执行了

```python
i=0
while i<10:
    i+=1
    if i%2==0:
        continue
    print(i
```

break 会执行后面的语句

while else
在while循环中的break能跳出else语句

对于while if 条件里面的变量一定要先赋一个初始值
break只能跳出一层循环

for 变量 In 可迭代对象：

打印乘法口诀表
```python
i=1
while i<=9:
    j=1
    while j<=i:
        print(j,"*",i,"=",i*j,end=" ")
        j+=1
    print()
    i+=1
```

```py
for each in "chei":
    print(each)
```

> len("获取一段代码长度")

range(stop)		从0开始到stop-1
range(start,stop)		从start到stop-1
range(start,stop,stop)		后面的stop是跨度

求素数

```py
for n in range(2,10):
    for x in range(2,n):
        if n%x==0:
            break
    else:
        print(n)
```

注意else的缩进，他与第二个for并列

### 列表

列表可以容纳不同的类型
列表也是个序列
可以通过下标指引，也是从零开始数，索引列表（最后一个值是-1，倒数第二个是-2）

### 列表切片

rhyme[3:6]		第四个开始到第六个
rhyme[3:]		第四个开始到最后
rhyme[:5]	最开始到第5个
rhyme[:]		全部
rhyme[0:6:2]	2是跨度
rhyme[::-1]	倒序输出

给列表增加一个数

```py
heros=["1","2"]
heros.append("3")
print(heros)
```

也可以直接加上一个可迭代对象
heros.extend(["4","5"])==heros[len(heros):]=[4,5]
heros.insert(1,2)		列表的第1+1个是2
heros.remove("1") 		删除“1”
heros.pop(2)		把第2+1个元素删除
heros.clear()		删除列表的所有元素
heros[4]="5"	把第五个元素改成“5”	
heros[3:]=["1","2","5"]		把第四个及后面的改了
变量.sort()		自动排序
变量。reverse()		倒序
变量。sort(reverse=Ture)	等于先sort再reverse
num.index("绿巨人")		索引值
。index（2，1，7）		在1号到7号元素中查找2
num.copy()	复制\=\=num[:]
列表的加法是拼接
s=[1,2,3]		s*3=[1,2,3,1,2,3,1,2,3]

### 嵌套列表

num[0]	第一行
num[0]\[0\]	第一行第一个
列表=[[]]*3			列表=[[],[],[]]		列表[0].append(3)----->列表=[[3],[3],[3]]	(这是引用不是复制)

```python
Python 3.15.1 (tags/v3.15.1:c37e74c, Oct 21 2026, 06:24:08) [MSC v.1951 64 bit (AMD64)] on win32
Enter "help" below or click "Help" above for more information.
a=[None]*3
for i in range(3):
    a[i]=[None]*2
print(a)
SyntaxError: invalid syntax
for i in range(3):
    a[i]=[None]*2

    
print(a)
[[None, None], [None, None], [None, None]]
a[0][0]=12
print(a)
[[12, None], [None, None], [None, None]]

```

若想创建多维列表可以这么做,这不再是引用，而是通过循环

```python
x=[1,2,3]
y=x
x[0]=5
print(y)
[5, 2, 3]
```

x,y不是两个独立的列表

### 浅拷贝（无法拷贝多维列表）

通过拷贝，可以得到两个独立的列表		y=x.copy()
也可以通过切片y=x[:]

```python
import copy
y=copy.copy(x)
```

### 深拷贝

> import copy
>
> y=copy.deepcopy(x)

### 列表推导式

>列表=[i*2 for i in 列表]

x=[i+1 for i in range(10)]

ord(c)		将单个字符串转换为对应的编码

s=[[0]*3 for i in range(3)]

even=[i for i in range(10) if i%2==0]		先for再if 最后i

### 元组

rhyme=（）

小括号或无括号
元组不可变
index查位置
.count(3)		数3出现了几次

生成一个只有一个元素的元组
x=(2,)

### 打包解包

a=1,2,3

x,y,z=a			----->x=1	y=2	z=3
元组中的元素是列表，因为列表可变这个元组也可以改变

capitalize	首字母大写

caseflod	全小写

title 	每个单词首字母大写，其他都是小写

swapcase  	大小写反转

upper () 	全大写

lower ()	全小写

center()	中对对齐

ljust()	左对齐

rjust()	右对齐

zfill()	在前面补0

ljust(15,"你")		15是字符长度	你是填充字符

find	找位置

rfind	从右边找位置

.expandtabs(4)		4表示4个空格，用空格替换tab

repalce("zaima","xaingni")	用想你替换在吗

### translate

>table=str.maketrans("ABCDEFG","1234567")
>
>再使用.translate能对应转化

startswith（“我是”）	是否以我开头

endswitch（“我是”）	是否以我结束

isupper	判断是否都是大写

isalpha		判断是否只有字母，就算是有空格也不行

isspace    判断是不是空白字符串

“我是\n”.isprintable() 		----->False   换行符不可以打印

.isidentifier()		判断是否是个合法的字符串（由数字，下划线，字母组成，不能以数字开头）

lstrip	 左侧不留白

rstrip	右侧不留白

strip	两侧不留白

strip("mococo")		去掉“内的包含的所有单个字符”只要出现一次无法去除的字符就马上停止

removeprefix		删除前缀
removesuffix			删除后缀

partition（分割标志）	分隔符
split()	分割空格

spilt（‘，’，1）		1表示只分割一次

splitlines		按照换行符分割

".",join(["www","132"])			用.来连接join内的字符串

### 格式化字符串

"{} is {}".format("saba","fish")		将后面的字符串填到{}中

"{0}{0}{1}{1}",format("是"，“非”)			是是非非

### 对齐

| 值   | 含义     |
| ---- | -------- |
| '<'  | 左对齐   |
| '>'  | 右对齐   |
| '^'  | 强制居中 |

"{:^10}".format(250)		

"{:010}".format(250)		用零填充

"{:%10}".format(250)		用百分号填充

{:,}.format(1234)		用逗号作为千分符

{:+}.format(1234)		正数用+121的形式表示

{:.2f}.format(3.1415)	小数点后两位精度

{:.2g}.format(3.1415)	限定小数点前后一共有多少数位

{:.7}.format(i love saba)		截取六位，

{:b}.format(90)		90的二进制

| b    | 二进制                   |
| ---- | ------------------------ |
| c    | unicode                  |
| d    | 十进制                   |
| o    | 八进制                   |
| x    | 十六进制                 |
| X    | 十六进制                 |
| e    | 科学计数法               |
| f    | 小数位数，默认为6        |
| g    | 小数以f输出，大数以e输出 |
| G    | 小数以F输出，大数以E输出 |
| %    | *100%                    |
|      |                          |

{:#b}.format(90)		90的二进制，添加#后，会有个表示类型的前缀

### f字符串

"{:^10}".format(250)			==		f"{250:^10}"

### del语句

del x[1:4]		x[1:4]=[]

### 序列

list()		列表
tuple		元组
str		字符串

大写的字母编码值是在小写的前面

```python
s=[]
min(s,default="空格怎么找最小值")
'空格怎么找最小值'
```

sorted()		返回的是新的函数

s.sorted()		这个时候s改变

reversed()		反转

sorted(s,revers=Ture)			先排序再倒序

sorted(t)		是一个字符串，比较完第一个后比较第二个字符，不论字符串长度
sorted(t,key=len)

all()	是否都为真
any()	是否有真

enumerate()	对可迭代对象都可以用（列表、元组）

```python
t=("a","b","c")
enumerate(t)
<enumerate object at 0x000002A870512890>
list(enumerate(t))
[(0, 'a'), (1, 'b'), (2, 'c')]
```

```python
x=[1,2,3]
y=[4,5,6]
list(zip(x,y))
						[(1,4),(2,5),(3,6)]
```

zip	若有字符串，只能输出最短的那个字符串
```python
import itertools
zipped=itertools.zip_longest(x,y)
		这是按照最长的字符串输出
```

ord		求出编码值

map	map是不是相当于zip后再进行某项运算

map(pow,[1,2,3],[4,5,6],[7,8,9])

filter		返回计算结果为真的结果

list(filter(str.lower,"FishC"))		只返回小写['i','s','h']

一个迭代器是一个可迭代对象，但是迭代器是一次性的

#### iter

```python
x=[1,2,3]
y=iter(x)
```

生成了对于x的迭代器
next是针对迭代器，依次提取一个元素

### 字典

映射关系中，字典由于序列

1. y={"saba":"fish","dooby":"mouse"}
   : 左边是键，右边是值。
   y["saba"]		输出'fish'
2. b=dict(saba="fish",dooby="mouse")         不能在键上加引号
3. 用列表c=dict([("saba","fish"),("dooby","mouse")])
4. c=dict({("saba":"fish"),("dooby":"mouse")})
5. c=dict({("saba":"fish"),("dooby":"mouse")},gura="shark")
6. c=dict(zip(["gura","dooby"],["fish","mouse"]))

#### fromkeys

```python
d=dict.fromkeys("fish",250)
d
{'f': 250, 'i': 250, 's': 250, 'h': 250}
```

d.pop('s')		返回s对应的值
d['c']=67		增加一个把c对应67的字典

d.popitem()	删除最后的元素
del d['i']	删除i的字典

d.clear()		把d变成空字典
d.update(F='70',C='60')		把F,C改了

d.get('c',"这里没有c")		把default 赋值
d.setdefault('c',"code")		如果没有c，会把c加入字典中

#### 视图对象

就是字典的动态视图，字典内容发生改变的时候，视图也会发生改变

keys	键的视图对象
values	值的视图对象

len(d)	字典中键的个数

对于迭代器e=iter(d)
			next(e)	迭代器只能走一遍

list(reversed(d))		字典也有顺序，所以能逆序（很老的python版本中，字典没有顺序）

#### 嵌套

d={"saba":{"math":60,"art":70}}

#### 列表推导式

b={v:k for k;k:v in d.items()}	把值与键交换

ord()		求编码值 

### 集合

集合中所有元素是唯一的，集合是无序的

#### 集合推导式

{s for s in "fishc"}		set就是集合的意思

set("fishc")		集合是无序的，不能用下标访问

因为集合有唯一性，可以用来去重		判断len(s)==len(set(s))	来判断是否含有重复元素

s.isdisjoint(set("JAVA"))		判断是否集合重合

判断是否是子集	s.issubset()
判断是否是超集：s.issuperset	超集如果B中的任意一个元素都是A中的元素那么，集合A是集合B的超集

并集 s.union
交集 ： s.intersection 
差集（所有属于A且不属于B的元素组成的集合，叫做A与B的差集）	s.difference

### frozenset

frozenset 	不可变

add是加入整个字符串，而不是单个的字符

### 可哈希

hash		整数的哈希是本身，浮点数的哈希值（如果能写成整数形式，如1.0，哈希值是1）
可哈希的对象通常是是不可变的

### 函数

pass	空语句，没意义

#### 形式参数、实际参数

函数中也能用return返回值，但是使用return后，程序就结束了
位置参数要在关键字参数前

```python
greet("Alice", age=20)   # ✅ 位置参数在前，关键字参数在后
```

#### 收集参数

（*args）		args=(1,2,3,4)
(\*\*args)			kwargs={'a':1,'b':2,'c':3}

#### 作用域

局部作用域：如果一个变量在函数里面，那么它就只能在函数中使用
全局作用域：在函数外定义一个变量

在函数中局部变量会覆盖全局变量

global:		global x		声明x是全局变量

nonlocal	能实现内部函数修改外部函数的值

| 层级            | 含义         | 例子                         |
| --------------- | ------------ | ---------------------------- |
| **L** Local     | 当前函数内部 | 函数参数、函数内赋值         |
| **E** Enclosing | 外层嵌套函数 | 闭包里的外层变量             |
| **G** Global    | 模块顶层     | 文件级变量                   |
| **B** Built-in  | Python 内置  | `print`、`len`、`ValueError` |

#### 闭包

==函数只有在定义和调用的时候需要加上小括号

嵌套函数，外层作用域的变量会保存，不会因为函数被调用就消失了

#### 装饰器

闭包，拿函数装参数

装饰器的调用顺序是从下到上
```python
@deco1
@deco2
@deco3
def func():
    pass
```

等价于

```python
func = deco1(deco2(deco3(func)))
```

先调用3然后2，1

### lambda表达式

lambda y:y*y

#### 生成器

保留数据的状态，支持next函数
生成器不支持下标索引
生成器表达式：不是一次性全部计算出来，而是一次次的计算

可以用函数的return来，写生成器

#### 递归

递归就是用自己，但是注意不要写成死循环，效率有点低，因为是一次次的计算
效率不如迭代

通过help()能查函数文档

类型注释：def times(a:str="fishc",n:int =3)->list		表示出要求输入和输出的值

内省：times.\_\_annotations\_\_	注意是两个下划线		类型注释

.\_\_doc\_\_	

lambda 是一种匿名函数，也就是不需要用 def 写完整函数名的小函数。

#### 高阶函数

reduce		要导入 import functools		
functools.reduce()		把可迭代对象，带入内层函数中

偏函数：partial

**偏函数就是把一个函数的部分参数提前固定，生成一个参数更少的新函数。**

@wraps装饰器： import functions

### 永久存储

open("fishc.txt","w")	w表示写入d, 	创建fishc.txt这个文档
f.write()		写入	（不包含换行符）
f.writelines	写入		（不包含换行符）
f.close		关闭文档，才能写入![屏幕截图 2026-11-07 173858](../../Pictures/Screenshots/屏幕截图 2026-11-07 173858.png)

flush可以在不关闭文件的情况下，写入

路径转换

* is_dir()	判断是否是文件夹

* is_file()	判断是否是文档

* ```python
  with open("fishc.txt","w") as f:
      f.write("i love fishc")
      1/0
  ```

  对于1/0这种会报错的情况，使用上述语句，能保证文件能够关闭

* pickle

### 异常

```python
try:
    1/0
except:
    print("逮到了")
else:
    print("没逮到")
finally:
    print("逮没逮到都会吱一声")
```

### 类和对象

在类里面定义的方法，第一个参数必须是 self

```python
class C:
    def hello(self):  # 加上 self
        print("你好~")

c = C()
c.hello()  # 正常运行，输出：你好~
```

class(类)是创建对象的蓝图

#### 继承

判断一个对象是否属于一个类			isinstance
检测一个类是不是某个类的子类 	issubclass

多重继承
访问顺序是从左往右的，如果在左边能找到就不会继续在右边寻找了 

组合：

self就是求值对象本身
self将实例对象和类的方法进行绑定

写空字典的时候可以

```python
class C:
    pass
c.C()
c.x=250
c.y="saba"
c.z=[1,2,3]
```

### 构造函数

\_\_init\_\_		初始化方法也是一种构造方法

super() 	能自动解决父类和子类的问题，super是根据mro的顺序的

mixin