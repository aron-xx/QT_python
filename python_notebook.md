#            python notebook

> **python 生成器**

```python
def fibo(n=0):
    a,b=0,1
    list_number=[0]
    for i in range(n):
        a,b = b,a+b  #并行处理，同时处理
        list_number.append(a)
    print(list_number)
def fibo(n):
    a,b=0,1
    for i in range(n):
        a,b=b,a+b
        yield a
for j in fibo():
    print(j)
  
        
```

> python 字符串的格式化(str)

```  python 
#'{{{name}}}'.format(name="xufang") input {name}
#'{{{{name}}}}'.format(name="xufang") input '{{}}'
#要针对格式化符号进行格式化时，当 {}时奇数对时，format内参数有效
#当{}时是偶数对时，format参数无效，只打印{}
width= int(input('please enter width:'))
price_width=10
item_width=width-price_width
header_fmt='{{:{}}}{{:>{}}}'.format(item_width,price_width)
fmt='{{:{}}}{{:>{}.2f}}'.format(item_width,price_width)
print('='*width)
print(header_fmt.format('Iterm','Price'))
print("-"*width)
print(fmt.format('Apple',0.4))
print(fmt.format('banana',0.6))
```



``` python
#Decorator
class Student():
    __slots__=('_name','_age')#限定student对象只能绑定name,age
    def __init__(self,name,age):
        self._name=name
        self._age=age
    @property  #使得Student对象能够以xxx.name方式访问
    def name(self):
        return self._name
    @name.setter#使得Student对象能够修改xxx.name属性
    def name(self,name):
        self._name=name
        
class M_S_Student(Student):
    def __init__(self,name,age,gender):
        super.().__init__(name,age)#继承父类，初始化继承父类的属性和方法
        self._gender=gender #子类只需增添一个新的属性，旧属性已经继承不需要再写
 #装饰器是当一个函数需要动态增加功能时，又不希望在函数内部修改代码，使得代码混乱，那么@语法就可以实现这种功能了
def a(func):
    ....
    def b():
        ....
        return func()
    return b
@a
def c():
    ...
    pass
#输出结果是：
#
```

``` python
#打印九九乘法口诀表
n=1
for i in range(1,10):
    while n <= i:
        print("{} × {} = {:2} ".format(n,i,n*i),end=" ")
        n +=1
    print("")
    n=1
    
```

