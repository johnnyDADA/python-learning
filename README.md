# python-learning
some notes about python-learning:

import random    # 导入产生随机数的模块
random.randint(1,10) #　产生一个1-10之间的随机整数
#coding:utf-8      #  可以输入中文字符

abs(10)  # 返回绝对值
max(a)  # 取出序列a中最大值
min(a)   # 取出序列a中最小值
len(a)    # 输出序列a的长度
 
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
cmp('hello','hello')  #判断第一个字符串与第二个字符串的大小关系
						    #若第一个大于第二个，返回1
							#小于第二个，返回-1
							#等于第二个，返回0
range(10)  >  [0,1,2,3,4,5,6,7,8,9]   # 快速生成一个序列

a="hello"
a.capitalize(a)  # 字符串首字母大写输出
a.replace("hello","good")  #替换全部内容
a.replace('l', 'x')  #将全部的 l  替换为  x  
a.replace('l' , 'x' ,1)  # 将第一个替换掉
a.split('h',1) > ['', 'ello']  #将  h  切割掉，并显示余下的内容

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

#猜字游戏
#coding:utf-8
import random
a=random.randint(1,10)
print a
print "let's play guess number game: "
guess=int(raw_input("input the number that you guess:"))
while guess != a:
    guess=int(raw_input("input the number that you guess:"))
    if guess > a:
        print "a little bigger"  
    if guess < a:
        print "a little smaller"
    if guess == a:
        print "bingo!"

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

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

#计算并输出任意位数的PAI:
#coding:utf-8
n = int(raw_input("请输入欲计算出的位数: "))
w = n+10
b = 10**w 
x1 = b*4//5 
x2 = b// -239 
he = x1+x2 
n *= 2 
for i in xrange(3,n,2):
    x1 //= -25 
    x2 //= -57121 
    x = (x1+x2) // i 
    he += x 
    pai = he*4 
    pai //= 10**10 
print pai 

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

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
