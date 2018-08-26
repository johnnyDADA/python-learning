# python-learning

some notes about python-learning:

常量 大写 BIRTH_OF_CHINA 类似的
input交互得到的都是 str 类型

import random    # 导入产生随机数的模块
random.randint(1,10) #　产生一个1-10之间的随机整数
#coding:utf-8      #  可以输入中文字符
range(1,5)  #产生1-4 4个整数
range(1,5,2)    #步长2，产生1,3两个整数

abs(10)  # 返回绝对值
max(a)  # 取出序列a中最大值
min(a)   # 取出序列a中最小值
len(a)    # 输出序列a的长度
 
type(a) #返回a的数据类型

def f(x):
	if x>5:
		return True
l=range(10)
l=[0,1,2,3,4,5,6,7,8,9]
filter(f,l) >  [6,7,8,9]   #起到过滤作用


divmod(10,3) > (3,1)   # 返回(10//3 , 10%3)
pow(10,3)  > 1000   #输出10的3次幂
round(10) > 10.0    #输出浮点值

callable(a)  #判断一个函数是否已经定义
isinstance (a,int)   # 判断变量a是否为int类型
isinstance(a,list)  #判断a是否是一个列表类型的量
cmp('hello','hello') 
                #判断第一个字符串与第二个字符串的大小关系
	        #若第一个大于第二个，返回1
		#小于第二个，返回-1
		#等于第二个，返回0
range(10)  >  [0,1,2,3,4,5,6,7,8,9]   # 快速生成一个序列

a="hello"
a.capitalize(a)  # 字符串首字母大写输出
a.swapcase(a)  #大小写翻转
a.center(10,#)  #字符串居中显示，一共10个字符大小，其他以 # 填充
a.replace("hello","good")  #替换全部内容
a.replace('l', 'x')  #将全部的 l  替换为  x  
a.replace('l' , 'x' ,1)  # 将第一个替换掉
a.split('h',1) > ['', 'ello']  #将  h  切割掉，并显示余下的内容
a.strip('')   #去除字符串中多余的空格只保留实际内容，可以知道去除的内容

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
180824
#猜字游戏
#coding:utf-8
import random
a=random.randint(1,10)
running=True
print (a)
print ("let's play guess number game, the number is between 1-10,have fun: ")
while running:
    guess=int(input("input the number that you guess:"))
    if guess == a:
        print ("bingo"  )
        running=False
    elif guess < a:
        print ("a little smaller")
    else:
        print ("a little bigger")


<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
161202
#输出斐波那契数列：
#coding:utf-8
def a(n):
    if n<=1:
        return n
    else:
        return ( a(n-1) + a(n-2) )
nterm=int(input("输入欲计算出的位数: "))
if nterm<=0:
    print("请输入正数")
else:
    for i in range(nterm):
        print(a(i))

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
161206
#计算并输出任意位数的PAI(不带小数点):
#coding:utf-8
n = int(input("请输入欲计算出的位数: "))
w = n+10
b = 10**w 
x1 = b*4//5 
x2 = b// -239 
he = x1+x2 
n *= 2 
for i in range(3,n,2):
    x1 //= -25 
    x2 //= -57121 
    x = (x1+x2) // i 
    he += x 
    pai = he*4 
    pai //= 10**10 
print (pai )

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
180824
#用字典的方式实现SWITCH功能
#!/usr/bin/python
#coding:utf-8
from __future__  import division
def jia(x,y):
	return x+y
def jian(x,y):
	return x-y
def cheng(x,y):
	return x*y
def chu(x,y):
	return x/y
operator = { "+":jia, "-":jian, "*":cheng, "/":chu }

def f(x,o,y):
	print operator.get(o)(x,y)

f(3,"+",2)
	
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
180820
+ 加 两个对象相加 3 + 5得到8。'a' + 'b'得到'ab'。
- 减 得到负数或是一个数减去另一个数 -5.2得到一个负数。50 - 24得到26。
* 乘 两个数相乘或是返回一个被重复若干次的字符串
    2 * 3得到6。'la' * 3得到'lalala'。
** 幂 返回x的y次幂 3 ** 4得到81（即3 * 3 * 3 * 3）
/ 除 x除以y 4/3得到1（整数的除法得到整数结果）。4.0/3或4/3.0得到1.3333333333333333
// 取整除 返回商的整数部分 4 // 3.0得到1.0
% 取模 返回除法的余数 8%3得到2。-25.5%2.25得到1.5
<< 左移把一个数的比特向左移一定数目（每个数在内存中都表示为比特或二进制数字，即0和1）
2 << 2得到8。——2按比特表示为10
>> 右移 把一个数的比特向右移一定数目 11 >> 1得到5。——11按比特表示为1011，向右移动1比特后得到101，即十进制的5。
& 按位与 数的按位与 5 & 3得到1。
| 按位或 数的按位或 5 | 3得到7。
^ 按位异或 数的按位异或 5 ^ 3得到6
~ 按位翻转 x的按位翻转是-(x+1) ~5得到6。
返回x是否小于y。所有比较运算符返回1
5 < 3返回0（即False）而3 < 5返回

< 小于
表示真，返回0表示假。这分别与特殊的变量True和False等价。注意，这些变量名的大写。
1（即True）。比较可以被任意连接：3
< 5 < 7返回True。
> 大于 返回x是否大于y
5 > 3返回True。如果两个操作数都是数字，它们首先被转换为一个共同的类型。否则，它总是返回False。
<= 小于等于 返回x是否小于等于y x = 3; y = 6; x <= y返回True。
>= 大于等于 返回x是否大于等于y x = 4; y = 3; x >= y返回True。
== 等于 比较对象是否相等
x = 2; y = 2; x == y返回True。x =
'str'; y = 'stR'; x == y返回False。x =
'str'; y = 'str'; x == y返回True。
!= 不等于 比较两个对象是否不相等 x = 2; y = 3; x != y返回True。
not 布尔“非”
如果x为True，返回False。如果x为
False，它返回True。
x = True; not y返回False。
and 布尔“与”
如果x为False，x and y返回False，否则它返回y的计算值。
x = False; y = True; x and y，由于x是False，返回False。在这里，Python不会计算y，因为它知道这个表达式的值肯定是False（因为x是False）。这个现象称为短路计算。
or 布尔“或” 如果x是True，它返回True，否则它返回y的计算值。
x = True; y = False; x or y返回True。短路计算在这里也适用

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<












