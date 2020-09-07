# -python-
【例子】比较的两个变量均指向可变类型。

a = ["hello"]

b = ["hello"]

print(a is b, a == b)  # False True

print(a is not b, a != b)  # True False

False True

True False

注意：
is, is not 对比的是两个变量的内存地址
==, != 对比的是两个变量的值
比较的两个变量，指向的都是地址不可变的类型（str等），那么is，is not 和 ==，！= 是完全等价的。
对比的两个变量，指向的是地址可变的类型（list，dict，tuple等），则两者是有区别的。


运算符的优先级

一元运算符优于二元运算符。例如3 ** -2等价于3 ** (-2)。

先算术运算，后移位运算，最后位运算。例如 1 << 3 + 2 & 7等价于 (1 << (3 + 2)) & 7。

逻辑运算最后结合。例如3 < 4 and 4 < 5等价于(3 < 4) and (4 < 5)。


数据类型与转换

整型
【例子】通过 print() 可看出 a 的值，以及类 (class) 是int。

a = 1031
print(a, type(a))

1031 <class 'int'>

【例子】使 1/3 保留 4 位，用 getcontext().prec 来调整精度。

decimal.getcontext().prec = 4

c = Decimal(1) / Decimal(3)

print(c)

0.3333

获取类型信息

获取类型信息 type(object)

【例子】


print(isinstance(1, int))  # True

print(isinstance(5.2, float))  # True

print(isinstance(True, bool))  # True

print(isinstance('5.2', str))  # True

注：
type() 不会认为子类是一种父类类型，不考虑继承关系。

isinstance() 会认为子类是一种父类类型，考虑继承关系。

如果要判断两个类型是否相同推荐使用 isinstance()。


类型转换

转换为整型 int(x, base=10)

转换为字符串 str(object='')

转换为浮点型 float(x)

【例子】

print(int('520'))  # 520

print(int(520.52))  # 520

print(float('520.52'))  # 520.52

print(float(520))  # 520.0

print(str(10 + 10))  # 20

print(str(10.1 + 5.2))  # 15.3



print() 函数





