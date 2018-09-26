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


数字和字符串都有小数据池
数字： -5 - 256 期间的数字，都只开辟一个内存空间 
字符串： 1、字符串内无特殊字符时，只开辟一个内存空间。
	

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
列表
b=['11','asa','ewew']
b.append('asass')   # 在列表最后新增一个元素
b.extend()  #在列表末尾新增一个列表，相当于扩容
b.insert(2,'sasaww')  # 在 'asa' 后新增一个元素，有索引，无返回值

b.pop(1)  # 删除'asa'元素，索引后的一位删除，有返回值。返回值为删除的元素 'asa'
b.pop()  #默认删除最后一个元素
b.remove('asa')  #直接删除元素
b.clear()  #清空列表
del b  #直接删除整个列表
del b[2]  #删除第二个元素
del b[0:2]  #删除 '11'  'asa' 切片删除，删除第0-1个元素

c=[1,2,3,6,7,5,4]
b.sort()  #正向排序  1-7
b.sort(reversr=True)  #逆向排序  7-1
b.reverse()   #反转   4576321

列表转换成字符串
join
print( ','.join([str(_) for _ in range(100, -1, -1)]))  #输出100,99,98,....,0  字符串
字符串转换成列表
s='qwer'
l=list(s)
print(l)  >  ['q', 'w', 'e', 'r', 't']

split
s='qwer'
l=s.split()
l=['qwer']

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

数值可变的数据类型:   list  dict  set 
 
数值不可变的数据类型:   int  bool  str  tuple

字典：

在循环一个字典或者列表的时候不能删除其中的数据  
元祖，集合，列表，当其中只有一个元素时需要加逗号，否则数据类型就是元素的本身类型（int,str....）


dic1={'age':18, 'name':'guo', 'sex':'male',}

增：
dic1['high'] = 185  #没有键值对，添加
dic1['age'] = 16  #有键值对，直接覆盖原有的

dic1.setdefault('weight', 100)  #没有添加，有的话不做更改

删：
dic1.pop('sex')  #删除 sex 键对应的数据，返回值为被删除的键值
dic1.pop('ss',None)   #删除不存在的数据时，不报错，返回设置的None值（这个可以随意设置返回的文字）
dic1.popitem()   #随机删除，返回被删除的元素，以元组形式
dic1.clear()   #清空字典
del dic1['name']  #无返回值

改：
dic1['age'] = 16  #有键值对，直接覆盖原有的

dic={'name':'jin', 'age':18, 'sex':male}
dic1={'name':'sa','weight':75}
dic1.update(dic)   #有的键值对覆盖，没有的在后面添加，dic不变，dic1有变化

查：
dic={'name':'jin', 'age':18, 'sex':male}
dic.keys()  #键
dic.values()  #值
dic.items()  #键值对，以列表形式
for i in dic:
    print(i)    #输出的是字典的键  

for k,v in dic:
    print(k,v)    #只打印键，值，以字符串的形式打印其具体值


<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

集合：
{}  可变数据类型，不过其里面的元素必须是不可变的数据类型（可哈希）

内部元素 无序，不重复

set={'alex', 'ww', 'saw'}
set1={'alex',3,4,5,6}

增：
set.add('sasas')
set.update('sasaaa')

删：
set.pop()  #随机删除元素，有返回值，返回值为被删除的元素	
set.remove('alex')  #按元素去删除
set.clear()  #清空
del set  #删除整个集合

交集： set & set1
并集： set | set1
反交集： set ^ set1  

用集合进行去重操作：
li=[1,2,3,3,4,5,6,6,66,5,4,1]
set1=set(li)
print(set1)
 {1,2,3,4,5,6,66,4}

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

文件操作
'r'：读

'w'：写

'a'：追加

'r+' == r+w（可读可写，文件若不存在就报错(IOError)）

'w+' == w+r（可读可写，文件若不存在就创建）

'a+' ==a+r（可追加可写，文件若不存在就创建）

读，只读，只写，追加
f = open('c:\\000\\1.txt', mode='r', encoding='utf-8')
content = f.read()
print(content)
f.close()

写： 不存在的文件，会直接创建一个文件,写入。
    若是已经存在的文件，则会覆盖原文件内容。
f.open('log', mode='w', encoding='utf-8')
f.write('sadas')
f.close()

追加： 在文件最后追加内容
f.open('log', mode='a', encoding='utf-8')
f.write('sadas')
f.close()

调整光标，实现从头读取文件,是按照字节定光标位置的，一个中文用3个字节去定位：
f.seek(0)

获取光标当前的位置：
f.tell()

读取一行数据
f.readline()

每一行当成列表中的一个元素，添加到列表中，一次性读取整个文件
f.readlines()

使用with语句可以不用写结尾的close
with open('log', mode='a', encoding='utf-8') as f:
    print(f.read())


<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<



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

<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

int :  bit_length   #返回位长
shop_cart = []
goods = [
{"name": "电脑", "price": 199},
{"name": "鼠标", "price": 100},
{"name": "游艇", "price": 200},
{"name": "美女", "price": 9999}
]

while 1:
    salary = input("请输入用户余额[quit结束]:")
    if salary.isdigit():
        salary = int(salary)
        break
    elif salary == "quit":
        exit("")
    else:
        print("please enter the number")

while 1:
    print("shop list".center(50, '*'))
    for  index, i in enumerate(goods):    #枚举列表中的元素以及下标以作为购买商品的ID号
        print(index, i)
    choose_number = input("请输入购买商品编号[quit结束]:")
    if choose_number.isdigit():
        choose_number = int(choose_number)
        shopping_list = []
        if 0 <= choose_number < len(goods):
            shopping_list.append(goods[choose_number])
            if salary >= shopping_list[0]["price"]:
              shop_cart.append(goods[choose_number])
              salary -= shopping_list[0]['price']
              print("当前购买的商品",shopping_list, "当前用户余额{salary}".format(salary=salary))
            else:
                print("余额不足")
        else:
            print("无效的商品choose_number.lower() 编号")
    elif choose_number == 'quit':

        print("购买的商品".center(50,"*"))
        for y in shop_cart:
            print(y)
        exit()
    else:
        print("无效的输入")



<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
#180904

import time
import sys

goods = [
    {'name': 'computer', 'price': 4399},
    {'name': 'watch',    'price': 1299},
    {'name': 'phone',    'price': 6399},
    {'name': 'car',      'price': 9999},
]

shop_cart = []

funccode = [
    {1: 'shopping car'},
    {2: 'crypto'}
]

count = 0
pwd0 = int(input('please set the password of system:'))
raw_pwd = pwd0 ^ 707128
print('''done, exit the system.....

''')

time.sleep(1)


pwd1 = int(input("welcome ,please input the password of DON's systme:"))
flag = ((pwd1 ^ 707128) == raw_pwd)

while not flag:
    pwd1 = int(input('sorry ,the password is wrong, please try again:'))
    if (pwd1 ^ 707128) != raw_pwd:
        print("sorry, you have tried but ur code isn't right, system shutdown..")
        sys.exit()
    else:
        pass
    break

choose = int(input('system login succeed, please select the funccode:'))

if choose == 1:
    while 1:
        salary = input("请输入用户余额[quit结束]:")
        if salary.isdigit():
            salary = int(salary)
            break
        elif salary == "quit":
            exit("")
        else:
            print("please enter the number")

    while 1:
        print()
        print("shop list".center(50, '*'))
        for index, i in enumerate(goods):  # 枚举列表中的元素以及下标以作为购买商品的ID号
            print(index, i)
        choose_number = input("请输入购买商品编号[quit结束]:")
        print()
        if choose_number.isdigit():
            choose_number = int(choose_number)
            shopping_list = []
            if 0 <= choose_number < len(goods):
                shopping_list.append(goods[choose_number])
                if salary >= shopping_list[0]["price"]:
                    shop_cart.append(goods[choose_number])
                    salary -= shopping_list[0]['price']
                    print("当前购买的商品", shopping_list, "当前用户余额{salary}".format(salary=salary))
                    print()
                else:
                    print("余额不足")
                    print()
            else:
                print("无效的商品choose_number.lower() 编号")
                print()
        elif choose_number == 'quit':

            print("购买的商品".center(50, "*"))
            print()
            for y in shop_cart:
                print(y)
                print()
            sys.exit()
        else:
            print("无效的输入")
            print()


<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<

#文件读写实现三次登录  180926
username = input('请输入你要注册的用户名：')
password = input('请输入你要注册的密码： ')

with open('list_of_info',mode='w',encoding='utf-8') as f:
    f.write('{}\n{}'.format(username,password))
print('恭喜你注册成功')

lis = []
i = 0
while i < 3:
    usn = input('请输入你的用户名：')
    pwd = input('请输入你的密码： ')
    with open('list_of_info',mode='r+',encoding='utf-8') as f1:
        for line in f1:
            lis.append(line)
    if usn == lis[0].strip() and pwd == lis[1].strip():
        print('登录成功')
        break
    else:print('用户名或密码错误，请重新输入')
    i+=1



<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<






