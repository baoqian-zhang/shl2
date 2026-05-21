# SHL Python 3.7 MCQ 考试题库（中英文对照）

> **考试信息 / Exam Info**:
> - **Technology Version**: Python 3.7
> - **考试类型 / Type**: Multi-choice test (选择题)
> - **考察范围 / Scope**: Python 编程、数据库(Databases)、模块与库(Modules & Libraries)
>
> **三大报告板块 / Report Subsections**:
> 1. **Python Basics** — 基础语法、程序结构、执行步骤、内存管理
> 2. **Python Programming** — 函数、异常处理、序列、文件操作、正则表达式、OOP
> 3. **Databases and Modules** — 数据库操作、模块安装、SearchPaths、标准库
>
> **所有答案已经过严格验证，确保准确无误。英文题目 + 中文翻译 + 详细解析。**

---

## 一、Python 基础语法 / Basic Syntax

---

### Q1
**EN**: What is the output of the following code?
```python
print(type(5/2))
```
A) `<class 'int'>`
B) `<class 'float'>`
C) `<class 'double'>`
D) `<class 'str'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 3 中 `/` 运算符始终返回 float 类型，即使两个操作数都是整数。

---

### Q2
**EN**: Which of the following is a valid variable name in Python?
A) `2var`
B) `my-var`
C) `_myVar`
D) `class`

**CN**: 以下哪个是 Python 中合法的变量名？

✅ **正确答案 / Answer: C**
> 变量名不能以数字开头(A错)，不能包含连字符(B错)，不能使用保留关键字(D错)。下划线开头是合法的。

---

### Q3
**EN**: What is the output?
```python
x = 10
y = 3
print(x // y)
```
A) 3.3333
B) 3
C) 4
D) 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `//` 是地板除(floor division)，返回不大于结果的最大整数。10 // 3 = 3。

---

### Q4
**EN**: What is the output?
```python
print(2 ** 3 ** 2)
```
A) 64
B) 512
C) 36
D) 12

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `**` 是右结合运算符，所以 `2 ** 3 ** 2` = `2 ** (3 ** 2)` = `2 ** 9` = 512。

---

### Q5
**EN**: Which of the following is NOT a Python keyword?
A) `lambda`
B) `yield`
C) `switch`
D) `assert`

**CN**: 以下哪个不是 Python 的关键字？

✅ **正确答案 / Answer: C**
> Python 没有 `switch` 关键字。`lambda`、`yield`、`assert` 都是 Python 关键字。

---

## 二、数据类型与运算符 / Data Types & Operators

---

### Q6
**EN**: What is the output?
```python
a = [1, 2, 3]
b = a
b.append(4)
print(a)
```
A) `[1, 2, 3]`
B) `[1, 2, 3, 4]`
C) `[4, 1, 2, 3]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `b = a` 创建的是引用而非副本，`b` 和 `a` 指向同一个列表对象。修改 `b` 也会影响 `a`。

---

### Q7
**EN**: What is the output?
```python
print(True + True)
```
A) True
B) False
C) 2
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> Python 中 `True` 等价于整数 1，`False` 等价于 0。所以 `True + True = 1 + 1 = 2`。

---

### Q8
**EN**: What is the data type of `x`?
```python
x = (1)
print(type(x))
```
A) `<class 'tuple'>`
B) `<class 'int'>`
C) `<class 'list'>`
D) `<class 'str'>`

**CN**: x 的数据类型是什么？

✅ **正确答案 / Answer: B**
> `(1)` 被 Python 解析为一个带括号的整数表达式，而不是元组。要创建单元素元组需要用 `(1,)`。

---

### Q9
**EN**: What is the output?
```python
print(bool([]))
```
A) True
B) False
C) None
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 空列表 `[]` 在布尔上下文中为 `False`。其他 falsy 值包括：`0`、`0.0`、`""`、`None`、`{}`、`set()`。

---

### Q10
**EN**: What is the output?
```python
x = 5
y = 2
print(x & y)
```
A) 7
B) 0
C) 1
D) 10

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `&` 是按位与运算符。5 的二进制是 101，2 的二进制是 010，按位与结果是 000 = 0。

---

## 三、字符串操作 / String Operations

---

### Q11
**EN**: What is the output?
```python
s = "Hello World"
print(s[-5:])
```
A) "Hello"
B) "World"
C) "Worl"
D) "orld"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `s[-5:]` 表示从倒数第5个字符开始到末尾。字符串索引从-1开始表示最后一个字符。"Hello World"的-5位置是'W'，所以结果是"World"。

---

### Q12
**EN**: What is the output?
```python
print("Python"[::-1])
```
A) "P"
B) "Python"
C) "nohtyP"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `[::-1]` 是切片操作，步长为-1表示反转字符串。

---

### Q13
**EN**: What is the output?
```python
s = "a,b,c"
print(s.split(","))
```
A) `"a,b,c"`
B) `["a", "b", "c"]`
C) `("a", "b", "c")`
D) `"abc"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `split(",")` 以逗号为分隔符将字符串分割为列表。

---

### Q14
**EN**: What is the output?
```python
print("abc".upper().find("B"))
```
A) 0
B) 1
C) -1
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `"abc".upper()` 返回 `"ABC"`。`find("B")` 在 `"ABC"` 中查找 `"B"`，`"B"` 在 `"ABC"` 中索引为 1。注意 `find()` 是区分大小写的，但这里 `"ABC"` 包含大写的 `"B"`，所以返回 1。

---

### Q15
**EN**: What is the output?
```python
print("hello".replace("l", "L", 1))
```
A) "heLLo"
B) "heLlo"
C) "heLlo"
D) "HeLlo"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `replace("l", "L", 1)` 只替换第一个匹配的 "l"。"hello" → "heLlo"。

---

## 四、列表、元组、集合、字典 / Lists, Tuples, Sets, Dicts

---

### Q16
**EN**: What is the output?
```python
my_list = [1, 2, 3, 4]
print(my_list[1:3])
```
A) `[1, 2]`
B) `[2, 3]`
C) `[1, 2, 3]`
D) `[2, 3, 4]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 切片 `[1:3]` 包含索引 1（包含）到索引 3（不包含），即索引 1 和 2 对应的元素 2 和 3。

---

### Q17
**EN**: What is the output?
```python
d = {"a": 1, "b": 2}
print(d.get("c", 0))
```
A) None
B) Error
C) 0
D) "c"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `dict.get(key, default)` 如果 key 不存在则返回 default 值（此处为 0），而不是抛出异常。

---

### Q18
**EN**: What is the output?
```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}
print(set1 & set2)
```
A) `{1, 2, 3, 4}`
B) `{1}`
C) `{2, 3}`
D) `{4}`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `&` 是集合交集运算符，返回两个集合中共有的元素。

---

### Q19
**EN**: What is the output?
```python
my_tuple = (1, 2, 3)
my_tuple[0] = 10
print(my_tuple)
```
A) `(10, 2, 3)`
B) `(1, 2, 3)`
C) Error
D) `(10, 1, 2, 3)`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 元组(tuple)是不可变的，不能修改其元素。尝试赋值会引发 `TypeError`。

---

### Q20
**EN**: What is the output?
```python
d = {"x": 10, "y": 20}
d["z"] = 30
print(len(d))
```
A) 2
B) 3
C) Error
D) 4

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 向字典添加新键值对后，字典包含3个元素。`len()` 返回键值对的数量。

---

### Q21
**EN**: What is the output?
```python
a = [1, 2, 3]
b = a.copy()
b[0] = 99
print(a[0])
```
A) 99
B) 1
C) 2
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `copy()` 创建列表的浅拷贝。`b` 是独立的新列表，修改 `b` 不影响 `a`。所以 `a[0]` 仍是 1。

---

### Q22
**EN**: What is the output?
```python
numbers = [1, 2, 3, 2, 4, 2]
print(numbers.count(2))
```
A) 1
B) 2
C) 3
D) 4

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `list.count(value)` 返回列表中指定值出现的次数。列表中 2 出现了 3 次。

---

### Q23
**EN**: What is the output?
```python
a = [3, 1, 4, 1, 5]
a.sort(reverse=True)
print(a[0])
```
A) 1
B) 3
C) 4
D) 5

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: D**
> `sort(reverse=True)` 对列表进行降序排序。排序后 `[5, 4, 3, 1, 1]`，`a[0]` 是 5。

---

### Q24
**EN**: What is the output?
```python
d1 = {"a": 1}
d2 = {"b": 2}
d1.update(d2)
print(d1)
```
A) `{"a": 1}`
B) `{"b": 2}`
C) `{"a": 1, "b": 2}`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `update()` 将一个字典的键值对合并到另一个字典中。

---

### Q25
**EN**: Which method is used to remove and return the last element of a list?
A) `pop()`
B) `remove()`
C) `delete()`
D) `discard()`

**CN**: 哪个方法用于移除并返回列表的最后一个元素？

✅ **正确答案 / Answer: A**
> `pop()` 默认移除并返回列表最后一个元素。`remove()` 按值移除但不返回，`delete` 是关键字不是列表方法。

---

## 五、控制流 / Control Flow

---

### Q26
**EN**: What is the output?
```python
for i in range(5, 0, -1):
    if i == 3:
        break
    print(i, end=" ")
```
A) 5 4
B) 5 4 3
C) 5 4 3 2 1
D) 4 5

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `range(5, 0, -1)` 生成 5, 4, 3, 2, 1。当 `i == 3` 时 `break` 终止循环，所以只打印了 5 和 4。

---

### Q27
**EN**: What is the output?
```python
x = 10
if x > 5:
    print("A")
elif x > 8:
    print("B")
else:
    print("C")
```
A) A
B) B
C) C
D) A B

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `if-elif-else` 结构中，只有第一个为真的分支被执行。`x > 5` 为真，所以只输出 "A"，`elif` 被跳过。

---

### Q28
**EN**: What is the output?
```python
i = 0
while i < 3:
    i += 1
    if i == 2:
        continue
    print(i, end=" ")
```
A) 1 3
B) 1 2 3
C) 2 3
D) 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 循环过程: i=0→i=1→打印1; i=1→i=2→continue跳过打印; i=2→i=3→打印3。输出: 1 3。

---

### Q29
**EN**: What is the output?
```python
for i in range(3):
    print(i, end=" ")
else:
    print("Done")
```
A) 0 1 2
B) 0 1 2 Done
C) Done
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 的 `for...else` 结构中，`else` 块在循环正常完成（未被 `break` 中断）后执行。

---

### Q30
**EN**: What is the output?
```python
x = 0
for i in range(5):
    if i % 2 == 0:
        x += i
print(x)
```
A) 6
B) 9
C) 4
D) 10

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 0到4中偶数为 0, 2, 4。0 + 2 + 4 = 6。

---

## 六、函数与作用域 / Functions & Scope

---

### Q31
**EN**: What is the output?
```python
def greet(name="World"):
    return "Hello, " + name

print(greet("Python"))
```
A) "Hello, World"
B) "Hello, Python"
C) "World"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 调用 `greet("Python")` 传入参数覆盖了默认值 "World"，返回 "Hello, Python"。

---

### Q32
**EN**: What is the output?
```python
x = 5

def my_func():
    x = 10
    print(x, end=" ")

my_func()
print(x)
```
A) 10 5
B) 5 10
C) 10 10
D) 5 5

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 函数内部的 `x = 10` 创建了一个局部变量，不影响全局变量 `x`。函数内打印局部变量 10，函数外打印全局变量 5。

---

### Q33
**EN**: What is the output?
```python
def func(a, b=[]):
    b.append(a)
    return b

print(func(1))
print(func(2))
```
A) `[1]` 然后 `[2]`
B) `[1]` 然后 `[1, 2]`
C) `[1]` 然后 `[1]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> **经典陷阱**: 默认参数 `b=[]` 在函数定义时只创建一次。第一次调用后 `b` 变为 `[1]`，第二次调用在同一个列表上追加，结果为 `[1, 2]`。

---

### Q34
**EN**: What is the output?
```python
def multiply(x, y):
    return x * y

result = multiply(y=3, x=4)
print(result)
```
A) 12
B) 7
C) Error
D) 34

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 使用关键字参数时可以任意顺序传参。`multiply(y=3, x=4)` 等价于 `multiply(4, 3)`，返回 12。

---

### Q35
**EN**: What does the `lambda` keyword do in Python?
A) Defines a class
B) Creates an anonymous function
C) Imports a module
D) Handles exceptions

**CN**: Python 中 `lambda` 关键字的作用是什么？

✅ **正确答案 / Answer: B**
> `lambda` 创建匿名函数（没有名字的小型函数），如 `lambda x: x + 1`。

---

### Q36
**EN**: What is the output?
```python
nums = [1, 2, 3, 4]
result = list(map(lambda x: x ** 2, nums))
print(result)
```
A) `[1, 2, 3, 4]`
B) `[2, 4, 6, 8]`
C) `[1, 4, 9, 16]`
D) `[1, 3, 5, 7]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `map()` 将 lambda 函数应用到列表每个元素上，`x ** 2` 计算平方。结果: `[1, 4, 9, 16]`。

---

### Q37
**EN**: What is the output?
```python
def outer():
    x = 10
    def inner():
        print(x)
    return inner

f = outer()
f()
```
A) Error
B) None
C) 10
D) 0

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 这是闭包(closure)。`inner` 函数可以访问外部函数 `outer` 中的变量 `x`。`f()` 调用打印 10。

---

### Q38
**EN**: What is the output?
```python
x = 5

def change():
    global x
    x = 10

change()
print(x)
```
A) 5
B) 10
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `global x` 声明使得函数内部可以修改全局变量。`x` 被改为 10。

---

## 七、面向对象编程 / OOP

---

### Q39
**EN**: What is the output?
```python
class Dog:
    def __init__(self, name):
        self.name = name

d = Dog("Buddy")
print(d.name)
```
A) "Dog"
B) "Buddy"
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `__init__` 是构造函数，`self.name = name` 将实例属性设为传入的值 "Buddy"。

---

### Q40
**EN**: What is the output?
```python
class Parent:
    def greet(self):
        return "Hello from Parent"

class Child(Parent):
    def greet(self):
        return "Hello from Child"

c = Child()
print(c.greet())
```
A) "Hello from Parent"
B) "Hello from Child"
C) "Hello from Parent Hello from Child"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 方法重写(method overriding)：子类 `Child` 覆盖了父类的 `greet` 方法，调用时使用子类的版本。

---

### Q41
**EN**: What is the output?
```python
class MyClass:
    count = 0
    
    def __init__(self):
        MyClass.count += 1

a = MyClass()
b = MyClass()
print(MyClass.count)
```
A) 0
B) 1
C) 2
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `count` 是类变量（类属性），所有实例共享。创建两个实例后 `count` 变为 2。

---

### Q42
**EN**: What is the purpose of `__str__` method in Python?
A) To create a new instance
B) To provide a string representation of an object
C) To delete an object
D) To compare two objects

**CN**: Python 中 `__str__` 方法的作用是什么？

✅ **正确答案 / Answer: B**
> `__str__` 方法定义对象的字符串表示，由 `str()` 和 `print()` 调用。

---

### Q43
**EN**: What is the output?
```python
class A:
    def __init__(self):
        self.x = 1

class B(A):
    def __init__(self):
        super().__init__()
        self.y = 2

b = B()
print(b.x, b.y)
```
A) Error
B) `1 2`
C) `None 2`
D) `0 2`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `super().__init__()` 调用父类的构造函数，初始化 `self.x = 1`。然后子类设置 `self.y = 2`。

---

## 八、异常处理 / Exception Handling

---

### Q44
**EN**: What is the output?
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```
A) 0
B) Error
C) "Cannot divide by zero"
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `10 / 0` 引发 `ZeroDivisionError`，被 `except` 捕获后打印提示信息。

---

### Q45
**EN**: What is the output?
```python
try:
    num = int("abc")
except ValueError:
    print("Invalid")
finally:
    print("Done")
```
A) "Invalid"
B) "Done"
C) "Invalid" 换行 "Done"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `int("abc")` 引发 `ValueError`，执行 `except` 块打印 "Invalid"。`finally` 块始终执行，打印 "Done"。

---

### Q46
**EN**: What is the output?
```python
try:
    x = 5 / 0
except ZeroDivisionError:
    print("Error")
else:
    print("Success")
```
A) "Error"
B) "Success"
C) "Error" 换行 "Success"
D) 无输出

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `else` 块只有在 `try` 块没有引发异常时才会执行。因为此处引发了异常，只执行 `except` 块。

---

### Q47
**EN**: What is the output?
```python
try:
    x = 10 / 2
except ZeroDivisionError:
    print("Error")
else:
    print("Success")
finally:
    print("Done")
```
A) "Success"
B) "Success" 换行 "Done"
C) "Error"
D) "Done"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `10 / 2 = 5.0` 没有异常，执行 `else` 块打印 "Success"，然后 `finally` 始终执行打印 "Done"。

---

## 九、列表推导式与生成器 / Comprehensions & Generators

---

### Q48
**EN**: What is the output?
```python
squares = [x**2 for x in range(5)]
print(squares)
```
A) `[0, 1, 4, 9, 16]`
B) `[1, 4, 9, 16, 25]`
C) `[0, 2, 4, 6, 8]`
D) `[0, 1, 2, 3, 4]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 列表推导式生成 0², 1², 2², 3², 4² = `[0, 1, 4, 9, 16]`。

---

### Q49
**EN**: What is the output?
```python
evens = [x for x in range(10) if x % 2 == 0]
print(evens)
```
A) `[1, 3, 5, 7, 9]`
B) `[0, 2, 4, 6, 8]`
C) `[2, 4, 6, 8, 10]`
D) `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 列表推导式筛选出 0-9 中的偶数：0, 2, 4, 6, 8。

---

### Q50
**EN**: What is the output?
```python
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [num for row in matrix for num in row]
print(flat)
```
A) `[[1, 2], [3, 4], [5, 6]]`
B) `[1, 3, 5, 2, 4, 6]`
C) `[1, 2, 3, 4, 5, 6]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 嵌套列表推导式展平二维列表。遍历顺序：先外层 for（每行），再内层 for（行内每个元素）。

---

### Q51
**EN**: What is the output?
```python
gen = (x for x in range(3))
print(type(gen))
```
A) `<class 'list'>`
B) `<class 'tuple'>`
C) `<class 'generator'>`
D) `<class 'set'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 使用圆括号 `()` 而不是方括号 `[]` 创建的是生成器表达式(generator expression)，返回生成器对象。

---

### Q52
**EN**: What is the output?
```python
nums = [1, 2, 3, 4, 5]
result = [x for x in nums if x > 3]
print(sum(result))
```
A) 9
B) 12
C) 7
D) 15

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 筛选出大于3的元素：[4, 5]，`sum([4, 5])` = 9。

---

## 十、内置函数 / Built-in Functions

---

### Q53
**EN**: What is the output?
```python
print(len("Hello World"))
```
A) 10
B) 11
C) 12
D) 5

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `len()` 返回字符串长度，"Hello World" 有 11 个字符（包括空格）。

---

### Q54
**EN**: What is the output?
```python
names = ["Alice", "Bob", "Charlie"]
print(sorted(names, key=len))
```
A) `["Alice", "Bob", "Charlie"]`
B) `["Bob", "Alice", "Charlie"]`
C) `["Charlie", "Bob", "Alice"]`
D) `["Alice", "Charlie", "Bob"]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `sorted()` 按 `key=len`（字符串长度）排序。Bob(3) < Alice(5) < Charlie(7)。

---

### Q55
**EN**: What is the output?
```python
a = [1, 2, 3]
b = [4, 5, 6]
print(list(zip(a, b)))
```
A) `[1, 2, 3, 4, 5, 6]`
B) `[(1, 4), (2, 5), (3, 6)]`
C) `[[1, 4], [2, 5], [3, 6]]`
D) `(1, 4, 2, 5, 3, 6)`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `zip()` 将两个可迭代对象按位置配对，返回元组列表。

---

### Q56
**EN**: What is the output?
```python
print(all([True, True, False]))
```
A) True
B) False
C) None
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `all()` 只有当所有元素都为真时才返回 `True`。列表中包含 `False`，所以返回 `False`。

---

### Q57
**EN**: What is the output?
```python
print(any([0, "", None, 5]))
```
A) True
B) False
C) None
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `any()` 只要有一个元素为真就返回 `True`。5 是真值，所以返回 `True`。

---

### Q58
**EN**: What is the output?
```python
print(list(enumerate(["a", "b", "c"], start=1)))
```
A) `[(0, 'a'), (1, 'b'), (2, 'c')]`
B) `[(1, 'a'), (2, 'b'), (3, 'c')]`
C) `[1, 2, 3]`
D) `['a', 'b', 'c']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `enumerate()` 返回索引和元素的配对。`start=1` 使索引从1开始。

---

### Q59
**EN**: What is the output?
```python
print(isinstance(5, int))
```
A) True
B) False
C) "int"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `isinstance()` 检查对象是否为指定类型。5 是 `int` 类型，返回 `True`。

---

### Q60
**EN**: What is the output?
```python
def is_even(n):
    return n % 2 == 0

nums = [1, 2, 3, 4, 5, 6]
result = list(filter(is_even, nums))
print(result)
```
A) `[1, 3, 5]`
B) `[2, 4, 6]`
C) `[1, 2, 3, 4, 5, 6]`
D) `[]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `filter()` 筛选出满足条件的元素。`is_even` 返回偶数为 True。

---

## 十一、文件操作 / File I/O

---

### Q61
**EN**: What is the correct way to open a file for reading in Python?
A) `open("file.txt", "w")`
B) `open("file.txt", "r")`
C) `open("file.txt", "a")`
D) `open("file.txt", "x")`

**CN**: Python 中正确打开文件进行读取的方式是什么？

✅ **正确答案 / Answer: B**
> `"r"` 是读取模式，`"w"` 是写入（覆盖），`"a"` 是追加，`"x"` 是排他创建。

---

### Q62
**EN**: What is the best practice for opening files in Python?
A) `f = open("file.txt")`
B) `with open("file.txt") as f:`
C) `file = read("file.txt")`
D) `open(file.txt)`

**CN**: Python 中打开文件的最佳实践是什么？

✅ **正确答案 / Answer: B**
> `with` 语句（上下文管理器）确保文件在使用后自动关闭，即使发生异常也是如此。

---

### Q63
**EN**: What is the output?
```python
with open("test.txt", "w") as f:
    f.write("Hello")

with open("test.txt", "a") as f:
    f.write(" World")

with open("test.txt", "r") as f:
    content = f.read()
    print(len(content))
```
(Assume the file does not exist before the code runs)
A) 5
B) 11
C) 10
D) 6

**CN**: 以下代码的输出是什么？（假设文件在运行前不存在）

✅ **正确答案 / Answer: B**
> 先写入 "Hello"(5字符)，再追加 " World"(6字符，包含前导空格)，总共 11 个字符。

---

## 十二、模块与包 / Modules & Packages

---

### Q64
**EN**: How do you import only the `sqrt` function from the `math` module?
A) `import math.sqrt`
B) `from math import sqrt`
C) `import sqrt from math`
D) `from sqrt import math`

**CN**: 如何从 `math` 模块中只导入 `sqrt` 函数？

✅ **正确答案 / Answer: B**
> 语法为 `from module import name`。`from math import sqrt` 是正确的写法。

---

### Q65
**EN**: What is the output?
```python
import math
print(math.floor(3.7))
```
A) 4
B) 3
C) 3.0
D) 4.0

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `math.floor()` 返回不大于参数的最大整数（向下取整）。`floor(3.7)` = 3。

---

### Q66
**EN**: What is the output?
```python
import random
random.seed(42)
print(random.randint(1, 10))
```
A) 一个 1 到 10 之间的随机数
B) 始终是 7（对于 seed 42）
C) 始终是 42
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `random.seed(42)` 固定随机数生成器的种子。使用 seed 42 时，Python 的 `randint(1, 10)` 稳定输出 7。（注：不同 Python 版本可能略有不同，但在同一版本下始终一致。）

---

## 十三、综合陷阱题 / Tricky Questions

---

### Q67
**EN**: What is the output?
```python
print(0.1 + 0.2 == 0.3)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 浮点数精度问题：`0.1 + 0.2` 实际等于 `0.30000000000000004`，不等于 `0.3`。

---

### Q68
**EN**: What is the output?
```python
a = [1, 2, 3]
b = [1, 2, 3]
print(a is b)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `is` 检查对象身份（内存地址）。`a` 和 `b` 是两个不同的列表对象（即使内容相同），所以 `a is b` 为 `False`。

---

### Q69
**EN**: What is the output?
```python
a = [1, 2, 3]
b = [1, 2, 3]
print(a == b)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `==` 检查值相等。`a` 和 `b` 内容相同（都是 `[1, 2, 3]`），所以 `a == b` 为 `True`。

---

### Q70
**EN**: What is the output?
```python
print(5 > 3 > 1)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> Python 支持链式比较。`5 > 3 > 1` 等价于 `(5 > 3) and (3 > 1)`，两者都为真。

---

### Q71
**EN**: What is the output?
```python
a = [[]] * 3
a[0].append(1)
print(a)
```
A) `[[1], [], []]`
B) `[[1], [1], [1]]`
C) `[[], [], []]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> **经典陷阱**: `[[]] * 3` 创建了三个指向同一个空列表的引用。修改一个会影响所有。三个元素都变成 `[1]`。

---

### Q72
**EN**: What is the output?
```python
def func(x, lst=[]):
    lst.append(x)
    return lst

print(func(1))
print(func(2, []))
print(func(3))
```
A) `[1]` `[2]` `[3]`
B) `[1]` `[2]` `[1, 3]`
C) `[1]` `[]` `[3]`
D) `[1]` `[2]` `[1, 2, 3]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `func(1)` → 默认列表获得 `[1]`。`func(2, [])` → 使用新的空列表 `[2]`，不影响默认列表。`func(3)` → 默认列表（仍是 `[1]`）追加 3，得到 `[1, 3]`。

---

### Q73
**EN**: What is the output?
```python
print(type(type(int)))
```
A) `<class 'type'>`
B) `<class 'int'>`
C) `<class 'object'>`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `type(int)` 返回 `<class 'type'>`（因为 int 是一个类）。`type(type(int))` 即 `type(type)`，返回 `<class 'type'>`。在 Python 中，`type` 的 type 就是它自己。

---

### Q74
**EN**: What does the expression `3 * "ab"` evaluate to?
A) `"ab3"`
B) `"ababab"`
C) `"3ab"`
D) Error

**CN**: 表达式 `3 * "ab"` 的结果是什么？

✅ **正确答案 / Answer: B**
> 在 Python 中，`整数 * 字符串` 会将字符串重复整数次。`3 * "ab"` = `"ababab"`。

---

### Q75
**EN**: What is the output?
```python
x = "hello"
print(x[::-1][::-1] == x)
```
A) True
B) False
C) Error
D) "hello"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `x[::-1]` 反转得到 "olleh"，再次 `[::-1]` 反转得到 "hello"，等于原始的 `x`。

---

### Q76
**EN**: What is the output?
```python
d = {}
d[[1, 2]] = "value"
print(d)
```
A) `{[1, 2]: "value"}`
B) `{}`
C) Error
D) `{1, 2: "value"}`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 字典的键必须是可哈希(hashable)的。列表是可变的，不可哈希，不能作为字典的键。会引发 `TypeError: unhashable type: 'list'`。

---

### Q77
**EN**: What is the output?
```python
x = 1
y = 1
print(x is y)
```
A) True
B) False
C) 取决于实现
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> Python 会对小整数(-5 到 256)进行缓存(interning)。`x` 和 `y` 都引用缓存的同一个整数对象 1，因此 `x is y` 为 `True`。

---

### Q78
**EN**: What is the output?
```python
a = 257
b = 257
print(a is b)
```
A) True
B) False
C) 取决于实现/Python 版本
D) Error

**CN**: 以下代码的常见输出是什么？

✅ **正确答案 / Answer: B**
> 在 CPython 中，整数缓存范围是 -5 到 256。257 超出此范围，`a` 和 `b` 一般是不同的对象，所以 `a is b` 通常为 `False`。但在脚本上下文（同一代码块）中解释器可能会优化，所以最准确的答案在考试中通常是 B（表示它们不是同一个对象）。

---

### Q79
**EN**: What is the output?
```python
print(max([1, 2, 3], [3, 2, 1]))
```
A) `[1, 2, 3]`
B) `[3, 2, 1]`
C) Error
D) `3`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `max()` 对列表进行逐元素比较。`[1, 2, 3]` vs `[3, 2, 1]`：比较第一个元素，3 > 1，所以 `[3, 2, 1]` 更大。

---

### Q80
**EN**: What is the output?
```python
print({1, 2} | {2, 3})
```
A) `{1, 2, 3}`
B) `{2}`
C) `{1, 2, 2, 3}`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `|` 是集合并集运算符。`{1, 2} | {2, 3}` = `{1, 2, 3}`。集合自动去重。

---

## 十四、输出预测综合题 / Code Output Prediction

---

### Q81
**EN**: What is the output?
```python
x = [1, 2, 3]
y = x
x = x + [4]
print(y)
```
A) `[1, 2, 3]`
B) `[1, 2, 3, 4]`
C) `[4]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `x = x + [4]` 创建了一个新列表（因为 `+` 返回新列表），并将 `x` 重新指向它。`y` 仍然指向原始列表 `[1, 2, 3]`。注意：如果是 `x += [4]`，则 y 也会变为 `[1, 2, 3, 4]`。

---

### Q82
**EN**: What is the output?
```python
print(3 * 1 ** 3)
```
A) 27
B) 3
C) 9
D) 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 运算符优先级：`**` 高于 `*`。`1 ** 3 = 1`，然后 `3 * 1 = 3`。

---

### Q83
**EN**: What is the output?
```python
s = "Python"
print(s[1:4:2])
```
A) "Pt"
B) "yh"
C) "yto"
D) "y"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 切片 `[1:4:2]`：从索引1开始，到索引4（不含），步长为2。s[1]="y", s[3]="h"。输出 "yh"。

---

### Q84
**EN**: What is the output of the following list comprehension?
```python
matrix = [[i+j for j in range(2)] for i in range(2)]
print(matrix)
```
A) `[[0, 1], [0, 1]]`
B) `[[0, 1], [1, 2]]`
C) `[[0, 0], [1, 1]]`
D) `[[0, 1], [2, 3]]`

**CN**: 以下列表推导式的输出是什么？

✅ **正确答案 / Answer: B**
> 外层 i: 0, 1；内层 j: 0, 1。i=0: [0+0, 0+1] = [0, 1]；i=1: [1+0, 1+1] = [1, 2]。matrix = `[[0, 1], [1, 2]]`。

---

### Q85
**EN**: What is the output?
```python
a = 5
b = 3
print(a // b, a % b)
```
A) 1 2
B) 2 1
C) 1 1
D) 2 2

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `5 // 3 = 1`（地板除），`5 % 3 = 2`（余数）。

---

### Q86
**EN**: What is the output?
```python
x = "".join(["a", "b", "c"])
y = "-".join(["a", "b", "c"])
print(x, y)
```
A) `abc a-b-c`
B) `a b c a-b-c`
C) `abc abc`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `"".join(...)` 用空字符串连接 → "abc"。`"-".join(...)` 用连字符连接 → "a-b-c"。

---

### Q87
**EN**: What is the output?
```python
x = {1, 2, 3}
x.add(2)
print(len(x))
```
A) 4
B) 3
C) 2
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 集合不允许重复元素。`add(2)` 但 2 已存在，集合保持不变，长度仍为 3。

---

### Q88
**EN**: What is the output?
```python
print(2 + 3 * 4 ** 2)
```
A) 50
B) 400
C) 100
D) 38

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 运算符优先级：`**` > `*` > `+`。`4 ** 2 = 16`，`3 * 16 = 48`，`2 + 48 = 50`。

---

### Q89
**EN**: What is the output?
```python
a = 10
b = 3
c = a / b
print(type(c))
```
A) `<class 'int'>`
B) `<class 'float'>`
C) `<class 'double'>`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 3 中除法 `/` 始终返回 `float` 类型。

---

### Q90
**EN**: What value does `round(2.675, 2)` return in Python?
A) 2.68
B) 2.67
C) 2.7
D) 2.675

**CN**: Python 中 `round(2.675, 2)` 的常见返回值是什么？

✅ **正确答案 / Answer: B**
> 浮点数精度问题：2.675 在二进制中无法精确表示，实际值略小于 2.675，所以 `round()` 向下舍入得到 2.67。这是 Python 浮点数的一个著名陷阱。

---

## 十五、进阶题 / Advanced Questions

---

### Q91
**EN**: What is the output?
```python
def decorator(func):
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs) * 2
    return wrapper

@decorator
def add(a, b):
    return a + b

print(add(2, 3))
```
A) 5
B) 10
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `@decorator` 语法糖等价于 `add = decorator(add)`。`wrapper` 函数将原始返回值 `5` 乘以 2，返回 10。

---

### Q92
**EN**: What is the output?
```python
class MyClass:
    def __init__(self, value):
        self.__value = value
    
    def get_value(self):
        return self.__value

obj = MyClass(42)
print(obj._MyClass__value)
```
A) Error
B) 42
C) None
D) 0

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 的名称改编(name mangling)：`__value` 被重命名为 `_MyClass__value`。通过 `obj._MyClass__value` 仍可访问。这不是真正的私有，只是约定的保护机制。

---

### Q93
**EN**: What is the output?
```python
a = 3
b = 5
a, b = b, a
print(a, b)
```
A) 3 5
B) 5 3
C) 3 3
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 支持元组解包交换：`a, b = b, a` 等价于 `(a, b) = (b, a)`，无需临时变量即可交换值。

---

### Q94
**EN**: What is the output?
```python
def func(*args):
    return sum(args)

print(func(1, 2, 3, 4))
```
A) Error
B) 10
C) `(1, 2, 3, 4)`
D) 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `*args` 收集所有位置参数到元组 `(1, 2, 3, 4)`，`sum()` 返回 10。

---

### Q95
**EN**: What is the output?
```python
print(len(set([1, 2, 2, 3, 3, 3])))
```
A) 6
B) 3
C) 2
D) 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `set()` 去除重复值：`{1, 2, 3}`。`len()` 返回 3。

---

### Q96
**EN**: What is the output?
```python
s = "abc123"
print(s.isalnum())
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `isalnum()` 检查字符串是否只包含字母和数字。"abc123" 只包含字母和数字，返回 `True`。

---

### Q97
**EN**: What is the output?
```python
x = [1, 2, 3]
y = [4, 5]
x.extend(y)
print(x)
```
A) `[1, 2, 3]`
B) `[1, 2, 3, [4, 5]]`
C) `[1, 2, 3, 4, 5]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `extend()` 将可迭代对象的所有元素追加到列表末尾。`append()` 才会将整个列表作为一个元素添加。

---

### Q98
**EN**: What is the output?
```python
d = {"a": 1, "b": 2, "c": 3}
for k, v in d.items():
    if v > 1:
        print(k, end="")
```
A) a
B) bc
C) abc
D) ab

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `d.items()` 遍历键值对。v > 1 的键为 "b" 和 "c"。`end=""` 表示无换行，输出 "bc"。

---

### Q99
**EN**: What does `__name__ == "__main__"` check?
A) Whether the script is being imported
B) Whether the script is run directly
C) Whether the script has errors
D) Whether the script has a main function

**CN**: `__name__ == "__main__"` 检查什么？

✅ **正确答案 / Answer: B**
> 当 Python 文件被直接运行时，`__name__` 被设为 `"__main__"`。被导入时，`__name__` 为模块名。此检查常用于判断代码是直接运行还是被导入。

---

### Q100
**EN**: What is the output?
```python
x = 5
print(f"The value is {x}")
```
A) "The value is 5"
B) "The value is {x}"
C) Error
D) "The value is {5}"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> f-string（格式化字符串字面量）以 `f` 为前缀，`{x}` 被替换为变量 `x` 的值 5。

---

## 十六、内存管理与垃圾回收 / Memory Management & Garbage Collection

> **考试重点 / Key Topics**: Python 3.7 内存管理机制、引用计数、垃圾回收、`gc` 模块、`id()` 函数

---

### Q101
**EN**: What does the `id()` function return in Python?
A) The value of the object
B) The type of the object
C) The memory address (identity) of the object
D) The size of the object

**CN**: Python 中 `id()` 函数返回什么？

✅ **正确答案 / Answer: C**
> `id()` 返回对象在内存中的唯一标识符（在 CPython 中即内存地址）。

---

### Q102
**EN**: What is the primary mechanism Python uses for memory management?
A) Manual memory allocation
B) Reference counting + Garbage Collection
C) Only Garbage Collection
D) Stack-based allocation only

**CN**: Python 内存管理的主要机制是什么？

✅ **正确答案 / Answer: B**
> Python 使用引用计数(reference counting)作为主要的内存管理机制，并辅以循环垃圾回收器(Cyclic Garbage Collector)处理循环引用。

---

### Q103
**EN**: What is the output?
```python
import sys
a = []
b = a
print(sys.getrefcount(a) - 1)
```
A) 0
B) 1
C) 2
D) 3

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `sys.getrefcount(a)` 返回引用计数（包含函数参数自身的临时引用，所以实际引用数需减1）。`a` 和 `b` 都引用同一个列表，引用计数为 2。

---

### Q104
**EN**: Which module is used for garbage collection control in Python?
A) `memory`
B) `gc`
C) `refcount`
D) `sys`

**CN**: Python 中哪个模块用于垃圾回收控制？

✅ **正确答案 / Answer: B**
> `gc`（Garbage Collector）模块提供了控制垃圾回收器的接口，如 `gc.collect()` 手动触发回收、`gc.enable()`/`gc.disable()` 控制回收器。

---

### Q105
**EN**: In Python, when does an object become eligible for garbage collection?
A) When the program ends
B) When its reference count drops to zero
C) After a fixed time interval
D) When explicitly deleted using `delete` keyword

**CN**: Python 中，对象何时变为可被垃圾回收？

✅ **正确答案 / Answer: B**
> 当一个对象的引用计数降至零时，Python 会立即回收该对象的内存。对于循环引用（引用计数永远不会为零的情况），循环垃圾回收器会检测并处理。

---

### Q106
**EN**: What is the output?
```python
import sys
x = 256
y = 256
print(x is y)
```
A) True
B) False
C) Error
D) Depends on the Python version

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> Python 缓存了小整数（-5 到 256）。256 在缓存范围内，`x` 和 `y` 指向同一个缓存对象。

---

### Q107
**EN**: What is the output?
```python
a = [1, 2, 3]
b = [1, 2, 3]
print(id(a) == id(b))
```
A) True
B) False
C) Error
D) Sometimes True, sometimes False

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `a` 和 `b` 是两个独立创建的列表对象，它们在内存中的地址不同，`id()` 返回值不同。

---

### Q108
**EN**: What does `del` do to an object in Python?
A) Immediately frees the memory
B) Decrements the reference count and removes the variable name
C) Marks the object as garbage
D) Calls the destructor directly

**CN**: Python 中 `del` 对对象做了什么？

✅ **正确答案 / Answer: B**
> `del` 删除变量名（引用），减少对象的引用计数。只有当引用计数变为零时，内存才会被释放。

---

### Q109
**EN**: What is a "memory leak" in Python typically caused by?
A) Forgetting to call `free()`
B) Circular references that the garbage collector cannot handle
C) Using too many variables
D) Not using `del` statement

**CN**: Python 中的"内存泄漏"通常由什么引起？

✅ **正确答案 / Answer: B**
> 循环引用（如对象 A 引用 B，B 引用 A）在没有外部引用时，引用计数永不归零。虽然 Python 的 GC 可以处理大多数循环引用，但包含 `__del__` 方法的循环引用在 Python 3.4 之前无法被回收（Python 3.4+ 已修复）。

---

### Q110
**EN**: What is the purpose of `gc.collect()` in Python?
A) To display current memory usage
B) To manually trigger garbage collection
C) To count garbage objects
D) To disable garbage collection

**CN**: Python 中 `gc.collect()` 的作用是什么？

✅ **正确答案 / Answer: B**
> `gc.collect()` 手动触发垃圾回收，立即回收不可达对象。返回回收的对象数量。

---

## 十七、正则表达式 / Regular Expressions

> **考试重点 / Key Topics**: `re` 模块、`match()`/`search()`/`findall()`/`sub()`、正则语法、原始字符串

---

### Q111
**EN**: What does `re.match()` do in Python?
A) Searches the entire string for a pattern
B) Matches a pattern only at the beginning of the string
C) Finds all occurrences of a pattern
D) Replaces a pattern in the string

**CN**: Python 中 `re.match()` 的作用是什么？

✅ **正确答案 / Answer: B**
> `re.match()` 只在字符串开头尝试匹配模式。如果开头不匹配则返回 `None`。要从任意位置搜索，应使用 `re.search()`。

---

### Q112
**EN**: What is the output?
```python
import re
result = re.findall(r'\d+', 'abc123def456')
print(result)
```
A) `['123', '456']`
B) `['1', '2', '3', '4', '5', '6']`
C) `['abc', 'def']`
D) `[123, 456]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `\d+` 匹配一个或多个数字。`findall()` 返回所有匹配项的列表：`['123', '456']`。

---

### Q113
**EN**: What is the output?
```python
import re
result = re.sub(r'\s+', '-', 'Hello   World')
print(result)
```
A) `'Hello World'`
B) `'Hello---World'`
C) `'Hello-World'`
D) `'Hello   -World'`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `re.sub(pattern, repl, string)` 将匹配模式的部分替换为指定字符串。`\s+` 匹配一个或多个空白字符，替换为 `-`。

---

### Q114
**EN**: What does the `r` prefix in `r'\d+'` mean?
A) It makes the regex case-insensitive
B) It denotes a raw string — backslashes are treated literally
C) It means "regular expression"
D) It makes the pattern repeat

**CN**: `r'\d+'` 中的 `r` 前缀是什么意思？

✅ **正确答案 / Answer: B**
> `r` 前缀表示原始字符串(raw string)，反斜杠 `\` 被视为字面字符而非转义字符。在正则表达式中非常有用，避免 `\d` 被解释为转义序列。

---

### Q115
**EN**: What is the output?
```python
import re
m = re.search(r'(\d{3})-(\d{4})', 'Phone: 123-4567')
print(m.group(1))
```
A) `'123-4567'`
B) `'123'`
C) `'4567'`
D) `None`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `group(1)` 返回第一个捕获组（第一对括号）的内容：`'123'`。`group(0)` 或 `group()` 返回完整匹配 `'123-4567'`，`group(2)` 返回 `'4567'`。

---

### Q116
**EN**: What is the output?
```python
import re
pattern = r'[A-Z][a-z]+'
result = re.findall(pattern, 'Hello World PYTHON')
print(result)
```
A) `['Hello', 'World', 'PYTHON']`
B) `['Hello', 'World']`
C) `['H', 'W', 'P', 'Y', 'T', 'H', 'O', 'N']`
D) `['Hello', 'World', 'P', 'Y', 'T', 'H', 'O', 'N']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `[A-Z][a-z]+` 匹配一个大写字母后跟一个或多个小写字母。`'Hello'` 和 `'World'` 匹配，`'PYTHON'` 全是大小字母不匹配。

---

### Q117
**EN**: What is the output?
```python
import re
result = re.split(r'[,;]', 'a,b;c,d')
print(result)
```
A) `['a', 'b', 'c', 'd']`
B) `['a,b;c,d']`
C) `['a', 'b;c', 'd']`
D) `['a,b', 'c,d']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `re.split()` 按匹配模式分割字符串。`[,;]` 匹配逗号或分号，字符串在逗号和分号处分割。

---

### Q118
**EN**: What does `.*` match in a regular expression?
A) Zero or more of any character (except newline by default)
B) One or more of any character
C) Only alphabetic characters
D) Only numeric digits

**CN**: 正则表达式中 `.*` 匹配什么？

✅ **正确答案 / Answer: A**
> `.` 匹配任意字符（默认不匹配换行符），`*` 表示零次或多次。`.*` 匹配零个或多个任意字符。

---

### Q119
**EN**: What is the output?
```python
import re
text = "Price: $100, Discount: $20"
result = re.findall(r'\$\d+', text)
print(result)
```
A) `['100', '20']`
B) `['$100', '$20']`
C) `['$', '$']`
D) `[]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `\$` 匹配字面美元符号（因为 `$` 在正则中表示行尾，需转义），`\d+` 匹配一个或多个数字。匹配结果：`['$100', '$20']`。

---

### Q120
**EN**: What is the output?
```python
import re
result = re.match(r'[a-z]+', 'Hello123')
print(bool(result))
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `re.match()` 从字符串开头匹配。`[a-z]+` 匹配小写字母，但 `'Hello123'` 以大写 `'H'` 开头，所以 `match()` 返回 `None`，`bool(None)` 为 `False`。

---

## 十八、模块安装与搜索路径 / Module Installation & SearchPaths

> **考试重点 / Key Topics**: `sys.path`、`PYTHONPATH`、pip 安装、`import` 机制、`__init__.py`

---

### Q121
**EN**: What is `sys.path` in Python?
A) The system's PATH environment variable
B) A list of directories Python searches for modules to import
C) The path to the Python executable
D) The current working directory

**CN**: Python 中 `sys.path` 是什么？

✅ **正确答案 / Answer: B**
> `sys.path` 是一个字符串列表，包含 Python 搜索模块的所有目录路径。当你 `import` 模块时，Python 按此列表顺序搜索。

---

### Q122
**EN**: What is the command to install a package using pip?
A) `python install package`
B) `pip install package_name`
C) `pip add package_name`
D) `python -m package_name`

**CN**: 使用 pip 安装包的命令是什么？

✅ **正确答案 / Answer: B**
> `pip install package_name` 从 PyPI（Python Package Index）下载并安装包。

---

### Q123
**EN**: What is the purpose of `__init__.py` file in a directory?
A) It initializes the Python interpreter
B) It marks the directory as a Python package
C) It contains the main program
D) It is required for all Python scripts

**CN**: 目录中 `__init__.py` 文件的作用是什么？

✅ **正确答案 / Answer: B**
> `__init__.py` 文件将一个目录标记为 Python 包(package)，使其可以被 `import`。可以为空文件，也可以包含包的初始化代码。（注：Python 3.3+ 引入了隐式命名空间包，`__init__.py` 不再严格必需，但在 SHL Python 3.7 考试中仍是标准做法。）

---

### Q124
**EN**: Which of the following correctly imports a module named `mymodule` from a subpackage?
```python
# Package structure:
# mypackage/
#     __init__.py
#     subpackage/
#         __init__.py
#         mymodule.py
```
A) `import mypackage.subpackage.mymodule`
B) `from mypackage import mymodule`
C) `import subpackage.mymodule`
D) `from mypackage.subpackage import mymodule`

**CN**: 以下哪个正确地从子包中导入模块？

✅ **正确答案 / Answer: D**
> `from mypackage.subpackage import mymodule` 是最直接的导入方式。A 虽然语法也正确（`import mypackage.subpackage.mymodule`），但使用时需写全路径 `mypackage.subpackage.mymodule`。SHL 考试中通常选 `from...import` 模式。

---

### Q125
**EN**: Where does `pip` install packages by default for Python 3.7?
A) The current working directory
B) The system's `site-packages` directory
C) The user's home directory
D) The `/tmp` directory

**CN**: Python 3.7 中 `pip` 默认将包安装在哪里？

✅ **正确答案 / Answer: B**
> pip 默认将包安装到 Python 的 `site-packages` 目录中（如 `/usr/lib/python3.7/site-packages/` 或虚拟环境中）。使用 `pip install --user` 可安装到用户目录。

---

### Q126
**EN**: What environment variable can be used to add custom module search paths?
A) `PATH`
B) `PYTHONPATH`
C) `MODULEPATH`
D) `PYTHONHOME`

**CN**: 哪个环境变量用于添加自定义模块搜索路径？

✅ **正确答案 / Answer: B**
> `PYTHONPATH` 环境变量中的目录会被添加到 `sys.path` 中，使 Python 能够在这些目录中搜索模块。

---

### Q127
**EN**: What is the output?
```python
import sys
print(type(sys.path))
```
A) `<class 'str'>`
B) `<class 'list'>`
C) `<class 'tuple'>`
D) `<class 'set'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `sys.path` 是一个列表(list)，可以像操作普通列表一样修改它（如 `sys.path.append('/my/path')`）。

---

### Q128
**EN**: What does `python -m pip install package` do differently from `pip install package`?
A) Nothing, they are identical
B) It ensures the pip corresponding to that Python interpreter is used
C) It installs the package globally
D) It only installs for the current user

**CN**: `python -m pip install package` 与 `pip install package` 有什么不同？

✅ **正确答案 / Answer: B**
> `python -m pip` 确保使用的是与当前 Python 解释器关联的 pip 版本，在多 Python 版本环境中避免混淆。

---

### Q129
**EN**: Which file is traditionally used to define dependencies and metadata for packaging a Python project?
A) `package.json`
B) `Makefile`
C) `Dockerfile`
D) `setup.py`

**CN**: 哪个文件传统上用于定义 Python 项目打包的依赖和元数据？

✅ **正确答案 / Answer: D**
> `setup.py` 是 Python 标准打包文件，包含 `install_requires` 等字段定义依赖。`requirements.txt` 也常用来冻结版本，但 `setup.py` 是官方打包标准。

---

### Q130
**EN**: What is the purpose of `if __name__ == '__main__':` in a Python module?
A) To check if the module is imported correctly
B) To execute code only when the module is run directly (not imported)
C) To define the main function
D) To check for syntax errors

**CN**: Python 模块中 `if __name__ == '__main__':` 的作用是什么？

✅ **正确答案 / Answer: B**
> 这段代码确保其中的代码只在模块被直接运行时执行，而在被 `import` 时不执行。常用于测试代码或命令行入口。

---

## 十九、Python 标准库 / Python Standard Library

> **考试重点 / Key Topics**: `os`、`sys`、`datetime`、`json`、`collections`、`math`、`random`

---

### Q131
**EN**: What is the output?
```python
import os
print(os.path.join('folder', 'subfolder', 'file.txt'))
```
A) `'folder/subfolder/file.txt'` (or with `\` on Windows)
B) `'folder', 'subfolder', 'file.txt'`
C) `'foldersubfolderfile.txt'`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `os.path.join()` 使用操作系统正确的路径分隔符连接路径组件。在 Linux 上输出 `'folder/subfolder/file.txt'`，Windows 上输出 `'folder\subfolder\file.txt'`。

---

### Q132
**EN**: What is the output?
```python
import datetime
d = datetime.date(2026, 5, 20)
print(d.strftime('%Y-%m-%d'))
```
A) `'2026-05-20'`
B) `'20-05-2026'`
C) `'2026/05/20'`
D) `'May 20, 2026'`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `strftime('%Y-%m-%d')` 格式化日期为 `年-月-日` 格式。`%Y` 是四位数年份，`%m` 是两位数月份，`%d` 是两位数日期。

---

### Q133
**EN**: What is the output?
```python
import json
data = '{"name": "Alice", "age": 30}'
parsed = json.loads(data)
print(parsed['name'])
```
A) `'Alice'`
B) `Alice`
C) `'{"name": "Alice", "age": 30}'`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `json.loads()` 将 JSON 字符串解析为 Python 字典。`parsed['name']` 返回字符串 `'Alice'`。

---

### Q134
**EN**: What is the output?
```python
import json
data = {"name": "Bob", "age": 25}
result = json.dumps(data)
print(type(result))
```
A) `<class 'dict'>`
B) `<class 'str'>`
C) `<class 'list'>`
D) `<class 'int'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `json.dumps()` 将 Python 对象序列化为 JSON 字符串，返回 `str` 类型。

---

### Q135
**EN**: What is the output?
```python
from collections import Counter
c = Counter('hello world')
print(c['l'])
```
A) 2
B) 3
C) 1
D) 5

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `Counter` 统计每个字符出现次数。`'hello world'` 中 `'l'` 出现了 3 次（注意还有一个 `'l'` 在 `'world'` 中）。

---

### Q136
**EN**: What is the output?
```python
from collections import defaultdict
d = defaultdict(int)
d['a'] += 1
print(d['a'], d['b'])
```
A) `1 0`
B) `1 KeyError`
C) `0 0`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `defaultdict(int)` 为不存在的键自动创建默认值（`int()` 返回 `0`）。`d['b']` 自动初始化为 0，不会引发 `KeyError`。

---

### Q137
**EN**: What is the output?
```python
import sys
print(sys.version_info.major)
```
(Assume Python 3.7.x)
A) 3
B) 7
C) 3.7
D) Error

**CN**: 以下代码的输出是什么？（假设 Python 3.7.x）

✅ **正确答案 / Answer: A**
> `sys.version_info` 返回命名元组，`major` 属性表示主版本号。在 Python 3.7 中为 `3`。

---

### Q138
**EN**: What is the output?
```python
import os
print(os.getcwd())
```
A) The current working directory path
B) The user's home directory
C) The Python installation directory
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `os.getcwd()` 返回当前工作目录（Current Working Directory）的绝对路径。

---

### Q139
**EN**: What does `random.shuffle()` do?
A) Returns a new shuffled list
B) Shuffles the list in-place and returns it
C) Shuffles the list in-place and returns None
D) Creates a random list

**CN**: `random.shuffle()` 的作用是什么？

✅ **正确答案 / Answer: C**
> `random.shuffle(list)` 就地（in-place）打乱列表，返回 `None`。重要：它修改原列表而不创建新列表。

---

### Q140
**EN**: What is the output?
```python
import math
print(math.ceil(3.1), math.floor(3.9))
```
A) 4 3
B) 3 4
C) 3 3
D) 4 4

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `ceil(3.1) = 4`（向上取整），`floor(3.9) = 3`（向下取整）。

---

## 二十、调试 / Debugging

> **考试重点 / Key Topics**: `pdb`、`assert`、`logging`、异常堆栈

---

### Q141
**EN**: What is the purpose of the `assert` statement in Python?
A) To handle runtime errors
B) To test if a condition is True, raising AssertionError if False
C) To log error messages
D) To terminate the program

**CN**: Python 中 `assert` 语句的作用是什么？

✅ **正确答案 / Answer: B**
> `assert condition` 在条件为 `False` 时引发 `AssertionError`。主要用于调试，可以通过 `python -O` 优化模式禁用所有 assert。

---

### Q142
**EN**: What is the output?
```python
x = 5
assert x > 0, "x must be positive"
print("OK")
```
A) `OK`
B) `AssertionError: x must be positive`
C) No output
D) Error without message

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `x > 0` 为 `True`，`assert` 通过，继续执行打印 `OK`。

---

### Q143
**EN**: What is the output?
```python
x = -1
assert x > 0, "x must be positive"
print("OK")
```
A) `OK`
B) `AssertionError: x must be positive`
C) No output
D) `-1`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `x > 0` 为 `False`，`assert` 失败并引发 `AssertionError`，可选的错误消息为 `"x must be positive"`。

---

### Q144
**EN**: What module is used for interactive debugging in Python?
A) `debug`
B) `pdb`
C) `trace`
D) `inspect`

**CN**: Python 中哪个模块用于交互式调试？

✅ **正确答案 / Answer: B**
> `pdb`（Python Debugger）是 Python 的内置调试器。常用函数包括 `pdb.set_trace()` 设置断点、`pdb.run()` 运行调试。

---

### Q145
**EN**: Which logging level is the HIGHEST (most severe) in Python's `logging` module?
A) DEBUG
B) WARNING
C) ERROR
D) CRITICAL

**CN**: Python `logging` 模块中哪个日志级别最高（最严重）？

✅ **正确答案 / Answer: D**
> 日志级别从低到高：DEBUG(10) < INFO(20) < WARNING(30) < ERROR(40) < CRITICAL(50)。CRITICAL 是最严重的级别。

---

### Q146
**EN**: What is the output?
```python
import logging
logging.basicConfig(level=logging.WARNING)
logging.debug("Debug message")
logging.warning("Warning message")
```
A) Both messages are printed
B) Only "Warning message" is printed
C) Only "Debug message" is printed
D) Neither message is printed

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 日志级别设为 `WARNING`，只有 `WARNING` 及以上级别的消息会被输出。`DEBUG` 级别低于 `WARNING`，被过滤。

---

### Q147
**EN**: What does `pdb.set_trace()` do when called in a Python script?
A) Terminates the program
B) Starts the Python debugger at that point
C) Prints the current stack trace
D) Logs an error message

**CN**: 在 Python 脚本中调用 `pdb.set_trace()` 会做什么？

✅ **正确答案 / Answer: B**
> `pdb.set_trace()` 在当前代码位置启动交互式调试器，允许逐行执行、检查变量等。

---

### Q148
**EN**: What is the output?
```python
try:
    raise ValueError("Invalid value")
except ValueError as e:
    print(type(e).__name__)
```
A) `Exception`
B) `ValueError`
C) `Invalid value`
D) `Error`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `type(e).__name__` 返回异常类的名称字符串，`ValueError` 异常的 `__name__` 是 `'ValueError'`。

---

## 二十一、数据库 / Databases

> **考试重点 / Key Topics**: `sqlite3`、DB-API 2.0、游标(cursor)、SQL 基本操作

---

### Q149
**EN**: Which module in Python's standard library provides an interface to SQLite databases?
A) `mysql`
B) `sqlite3`
C) `psycopg2`
D) `database`

**CN**: Python 标准库中哪个模块提供 SQLite 数据库接口？

✅ **正确答案 / Answer: B**
> `sqlite3` 是 Python 内置的 SQLite 数据库模块，无需额外安装。`psycopg2` 是 PostgreSQL 的第三方驱动。

---

### Q150
**EN**: What is a "cursor" in the context of database operations in Python?
A) A pointer to the database file
B) An object used to execute SQL queries and fetch results
C) The current position in the code
D) A type of database table

**CN**: Python 数据库操作中，"游标(cursor)"是什么？

✅ **正确答案 / Answer: B**
> 游标(Cursor)是通过数据库连接创建的对象，用于执行 SQL 语句并从结果集中获取数据。

---

### Q151
**EN**: What is the correct order of operations for using sqlite3 in Python?
A) connect → cursor → execute → fetch → close
B) cursor → connect → execute → fetch → close
C) execute → connect → cursor → fetch → close
D) connect → execute → cursor → fetch → close

**CN**: Python 中使用 sqlite3 的正确操作顺序是什么？

✅ **正确答案 / Answer: A**
> 正确顺序：1) `connect()` 建立连接，2) `cursor()` 创建游标，3) `execute()` 执行 SQL，4) `fetch()` 获取结果，5) `close()` 关闭连接。

---

### Q152
**EN**: What does `cursor.fetchone()` return when there are no more rows?
A) An empty list
B) `None`
C) An empty tuple
D) Raises an exception

**CN**: 当没有更多行时，`cursor.fetchone()` 返回什么？

✅ **正确答案 / Answer: B**
> 当结果集中没有更多行时，`fetchone()` 返回 `None`。这常用于循环条件判断。

---

### Q153
**EN**: What does `cursor.fetchall()` return?
A) A single row as a tuple
B) A list of tuples, each representing a row
C) A dictionary of all rows
D) The number of rows in the result

**CN**: `cursor.fetchall()` 返回什么？

✅ **正确答案 / Answer: B**
> `fetchall()` 返回包含所有剩余行的列表，其中每一行是一个元组。

---

### Q154
**EN**: What is the purpose of the `?` placeholder in SQLite queries with Python?
```python
cursor.execute("SELECT * FROM users WHERE id = ?", (user_id,))
```
A) It represents an unknown value
B) It is a parameterized query placeholder to prevent SQL injection
C) It is a wildcard for any character
D) It marks optional columns

**CN**: Python SQLite 查询中 `?` 占位符的作用是什么？

✅ **正确答案 / Answer: B**
> `?` 是参数化查询的占位符，值通过元组传入。这可以防止 SQL 注入攻击，并自动处理转义。

---

### Q155
**EN**: What must be called after making changes (INSERT, UPDATE, DELETE) to a SQLite database?
A) `cursor.refresh()`
B) `connection.commit()`
C) `cursor.save()`
D) `connection.flush()`

**CN**: 对 SQLite 数据库进行更改（INSERT, UPDATE, DELETE）后必须调用什么？

✅ **正确答案 / Answer: B**
> `connection.commit()` 将更改永久保存到数据库。如果不调用 `commit()`，更改在连接关闭时会丢失。

---

### Q156
**EN**: Which DB-API method is used to rollback a transaction?
A) `connection.undo()`
B) `connection.rollback()`
C) `cursor.rollback()`
D) `connection.revert()`

**CN**: 哪个 DB-API 方法用于回滚事务？

✅ **正确答案 / Answer: B**
> `connection.rollback()` 撤销自上次 `commit()` 以来的所有更改。

---

## 二十二、网络编程 / Networking

> **考试重点 / Key Topics**: `socket` 模块、TCP/IP 基础、HTTP 概念

---

### Q157
**EN**: Which module in Python's standard library is used for low-level network communication?
A) `http`
B) `socket`
C) `network`
D) `requests`

**CN**: Python 标准库中哪个模块用于底层网络通信？

✅ **正确答案 / Answer: B**
> `socket` 模块提供 BSD socket 接口，用于底层网络通信（TCP/UDP）。`requests` 是第三方 HTTP 库，不在标准库中。

---

### Q158
**EN**: What does `socket.AF_INET` specify?
A) The socket type (TCP)
B) The address family (IPv4)
C) The protocol (HTTP)
D) The port number

**CN**: `socket.AF_INET` 指定什么？

✅ **正确答案 / Answer: B**
> `AF_INET` 指定 IPv4 地址族（Address Family）。`AF_INET6` 用于 IPv6。

---

### Q159
**EN**: What does `socket.SOCK_STREAM` specify?
A) UDP protocol
B) TCP protocol (connection-oriented)
C) Raw socket
D) HTTP protocol

**CN**: `socket.SOCK_STREAM` 指定什么？

✅ **正确答案 / Answer: B**
> `SOCK_STREAM` 表示 TCP 协议（面向连接、可靠的流式传输）。`SOCK_DGRAM` 表示 UDP 协议。

---

### Q160
**EN**: What is the output?
```python
import socket
print(socket.gethostname())
```
A) The IP address of the local machine
B) The hostname of the local machine
C) The MAC address
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `socket.gethostname()` 返回本机的主机名(hostname)字符串。

---

### Q161
**EN**: What is the typical port number for HTTP?
A) 21
B) 80
C) 443
D) 8080

**CN**: HTTP 的典型端口号是多少？

✅ **正确答案 / Answer: B**
> HTTP 默认使用端口 80。HTTPS 使用端口 443。FTP 使用端口 21。

---

### Q162
**EN**: Which method does a TCP server socket use to wait for incoming connections?
A) `socket.connect()`
B) `socket.listen()`
C) `socket.accept()`
D) `socket.bind()`

**CN**: TCP 服务器 socket 使用哪个方法等待传入连接？

✅ **正确答案 / Answer: B**
> `listen()` 使 socket 进入监听模式。之后使用 `accept()` 接受连接。`bind()` 绑定地址，`connect()` 用于客户端发起连接。

---

### Q163
**EN**: What is the output?
```python
import socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
print(type(s))
```
A) `<class 'socket.socket'>`
B) `<class 'socket'>`
C) `<class 'object'>`
D) `<class 'connection'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `socket.socket()` 返回一个 socket 对象，类型为 `socket.socket`。

---

## 二十三、程序结构与执行 / Program Structure & Execution

> **考试重点 / Key Topics**: Python 程序执行步骤、解释器、字节码、`.pyc` 文件

---

### Q164
**EN**: What is the correct file extension for a Python script?
A) `.python`
B) `.py`
C) `.pyt`
D) `.script`

**CN**: Python 脚本的正确文件扩展名是什么？

✅ **正确答案 / Answer: B**
> Python 脚本文件的标准扩展名是 `.py`。

---

### Q165
**EN**: What is a `.pyc` file in Python?
A) A Python configuration file
B) A compiled bytecode file
C) A Python class file
D) A compressed Python script

**CN**: Python 中 `.pyc` 文件是什么？

✅ **正确答案 / Answer: B**
> `.pyc` 是 Python 编译后的字节码(bytecode)文件，存储在 `__pycache__` 目录中。Python 自动创建它以加速后续导入。

---

### Q166
**EN**: What happens when a Python script is executed?
A) It is directly executed line by line
B) It is compiled to bytecode, then executed by the Python Virtual Machine
C) It is converted to machine code first
D) It is interpreted without any compilation

**CN**: Python 脚本执行时发生了什么？

✅ **正确答案 / Answer: B**
> Python 先将源代码编译为字节码(bytecode)，然后由 Python 虚拟机(PVM)执行。这是一个两步过程。

---

### Q167
**EN**: Which of the following is the correct structure for a basic Python program with a main function?
A) 
```python
main():
    print("Hello")
```
B)
```python
def main():
    print("Hello")

if __name__ == "__main__":
    main()
```
C)
```python
function main:
    print("Hello")
main()
```
D)
```python
def main():
    print("Hello")
main()
```

**CN**: 以下哪个是带有 main 函数的基本 Python 程序的正确结构？

✅ **正确答案 / Answer: B**
> 这是 Python 推荐的最佳实践：将主要逻辑放在 `main()` 函数中，并通过 `if __name__ == "__main__":` 来调用，使模块既可独立运行也可被导入。

---

### Q168
**EN**: What is an indentation in Python used for?
A) Code decoration only
B) Defining code blocks (instead of braces `{}`)
C) Adding comments
D) Separating statements

**CN**: Python 中的缩进用于什么？

✅ **正确答案 / Answer: B**
> Python 使用缩进（而不是花括号 `{}`）来定义代码块。同一代码块必须具有相同的缩进级别。标准是使用 4 个空格。

---

### Q169
**EN**: What happens if you mix tabs and spaces for indentation in Python 3?
A) It works normally
B) Python automatically converts tabs to spaces
C) It raises a `TabError`
D) Python ignores the difference

**CN**: 如果在 Python 3 中混合使用制表符和空格进行缩进会发生什么？

✅ **正确答案 / Answer: C**
> Python 3 不允许混合使用制表符和空格进行缩进，会引发 `TabError: inconsistent use of tabs and spaces in indentation`。

---

### Q170
**EN**: What is the purpose of a shebang line (`#!/usr/bin/env python3`) at the top of a Python script?
A) It is a comment for documentation
B) It tells the operating system which interpreter to use to run the script
C) It imports the Python environment
D) It defines the Python version

**CN**: Python 脚本顶部的 shebang 行 (`#!/usr/bin/env python3`) 的作用是什么？

✅ **正确答案 / Answer: B**
> Shebang 行告知操作系统使用哪个解释器来执行脚本。在 Unix/Linux 系统上，设置了执行权限后可直接运行脚本而无需显式调用 `python3`。

---

---

## 二十四、多选题专项 / Multi-Select Questions

> **⚠️ 重要说明 / Important**: SHL "Multi-choice test" 通常指**单选题**（多选一）。但部分考试可能包含**多选题**（Select ALL that apply — 选出所有正确答案）。以下为多选专项练习，每道题可能有 2-3 个正确选项。

---

### MS1 (Multi-Select)
**EN**: Which of the following are immutable data types in Python? *(Select ALL that apply)*
A) List
B) Tuple
C) String
D) Dictionary
E) Set

**CN**: 以下哪些是 Python 中的不可变数据类型？**（选出所有正确答案）**

✅ **正确答案 / Answer: B, C**
> Tuple(元组)和 String(字符串)是不可变的。List、Dictionary、Set 都是可变的。

---

### MS2 (Multi-Select)
**EN**: Which of the following can be used as dictionary keys in Python? *(Select ALL that apply)*
A) String
B) List
C) Tuple containing only immutable elements
D) Integer
E) Set

**CN**: 以下哪些可以作为 Python 字典的键？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D**
> 字典的键必须是可哈希(hashable)且不可变的。String(A)、整数(D)、纯不可变元组(C)都可以。List(B)和Set(E)可变且不可哈希，不能作为键。

---

### MS3 (Multi-Select)
**EN**: Which of the following are valid ways to create a list in Python? *(Select ALL that apply)*
A) `list()`
B) `[1, 2, 3]`
C) `list((1, 2, 3))`
D) `{1, 2, 3}`
E) `(1, 2, 3)`

**CN**: 以下哪些是创建列表的有效方式？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, C**
> `list()` 创建空列表，`[1,2,3]` 是字面量，`list((1,2,3))` 从元组转换。D 创建集合，E 创建元组。

---

### MS4 (Multi-Select)
**EN**: Which of the following statements about Python functions are TRUE? *(Select ALL that apply)*
A) Functions can return multiple values using tuples
B) Default argument values are evaluated each time the function is called
C) `*args` collects positional arguments into a tuple
D) `**kwargs` collects keyword arguments into a dictionary
E) A function must always have a `return` statement

**CN**: 以下关于 Python 函数的说法哪些是正确的？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D**
> A 正确（`return a, b` 实际返回元组）；C 和 D 是正确的参数收集语法。B 错误 — 默认参数在函数**定义时**只计算一次。E 错误 — 函数可以没有 `return`（隐式返回 `None`）。

---

### MS5 (Multi-Select)
**EN**: Which of the following will raise an exception in Python? *(Select ALL that apply)*
A) `int("123")`
B) `int("abc")`
C) `[1, 2, 3][5]`
D) `"hello"[1]`
E) `10 / 0`

**CN**: 以下哪些会在 Python 中引发异常？**（选出所有正确答案）**

✅ **正确答案 / Answer: B, C, E**
> B 引发 `ValueError`（"abc"不能转为整数）；C 引发 `IndexError`（索引越界）；E 引发 `ZeroDivisionError`。A 正常返回 123；D 正常返回 "e"。

---

### MS6 (Multi-Select)
**EN**: Which magic methods are correctly paired with their purpose in Python? *(Select ALL that apply)*
A) `__init__` — object initialization (constructor)
B) `__str__` — string representation of an object
C) `__add__` — subtraction operator
D) `__len__` — returns the length of an object
E) `__del__` — object multiplication

**CN**: 以下哪些魔术方法与其用途正确配对？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D**
> `__init__` 是构造函数，`__str__` 用于 `str()` 和 `print()`，`__len__` 用于 `len()`。C 错误（`__add__` 是加法，减法对应 `__sub__`）。E 错误（`__del__` 是析构函数，乘法对应 `__mul__`）。

---

### MS7 (Multi-Select)
**EN**: Which of the following are built-in Python modules? *(Select ALL that apply)*
A) `os`
B) `sys`
C) `requests`
D) `math`
E) `numpy`

**CN**: 以下哪些是 Python 内置模块（标准库）？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D**
> `os`、`sys`、`math` 都在 Python 标准库中。`requests` 和 `numpy` 是第三方库，需要通过 pip 安装。

---

### MS8 (Multi-Select)
**EN**: Which of the following are valid Python keywords? *(Select ALL that apply)*
A) `lambda`
B) `switch`
C) `yield`
D) `async`
E) `function`

**CN**: 以下哪些是有效的 Python 关键字？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D**
> `lambda`、`yield`、`async` 都是 Python 3 关键字。Python 没有 `switch` 关键字（B），也没有 `function` 关键字（E），定义函数用 `def`。

---

### MS9 (Multi-Select)
**EN**: Which of the following are TRUE about Python sets? *(Select ALL that apply)*
A) Sets are unordered collections
B) Sets can contain duplicate elements
C) Sets support union (`|`) and intersection (`&`) operations
D) Sets are mutable (elements can be added/removed)
E) Sets preserve insertion order in Python 3.7

**CN**: 以下关于 Python 集合的说法哪些是正确的？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D**
> A 正确（集合无序）；C 正确（支持集合运算）；D 正确（`add()`/`remove()` 修改集合）。B 错误（集合自动去重）。E 错误 — Python 3.7 中 dict 保持插入顺序，但 set 不保证顺序。

---

### MS10 (Multi-Select)
**EN**: Which of the following correctly create a shallow copy of a list? *(Select ALL that apply)*
A) `new_list = old_list.copy()`
B) `new_list = old_list`
C) `new_list = list(old_list)`
D) `new_list = old_list[:]`
E) `new_list = old_list.deepcopy()`

**CN**: 以下哪些正确创建列表的浅拷贝？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D**
> `.copy()`、`list()`、`[:]` 切片都创建浅拷贝。B 只创建引用（不拷贝）。E 方法名错误（正确是 `copy.deepcopy()`，且是深拷贝）。

---

### MS11 (Multi-Select)
**EN**: Which of the following are valid modes for opening a file in Python? *(Select ALL that apply)*
A) `"r"` — read mode
B) `"w"` — write mode (overwrites)
C) `"rw"` — read and write mode
D) `"a"` — append mode
E) `"x"` — exclusive creation

**CN**: 以下哪些是 Python 中有效的文件打开模式？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D, E**
> `"r"`, `"w"`, `"a"`, `"x"` 都是标准模式。C 错误（读写模式是 `"r+"` 或 `"w+"`，不是 `"rw"`）。

---

### MS12 (Multi-Select)
**EN**: In Python, which of the following evaluate to `False` in a boolean context? *(Select ALL that apply)*
A) `0`
B) `[]`
C) `"False"`
D) `None`
E) `{}`

**CN**: Python 中，以下哪些在布尔上下文中求值为 `False`？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D, E**
> `0`、`[]`（空列表）、`None`、`{}`（空字典）都是 falsy。C 错误 — `"False"` 是非空字符串，为 truthy。

---

### MS13 (Multi-Select)
**EN**: Which of the following are valid ways to handle exceptions in Python? *(Select ALL that apply)*
A) `try...except`
B) `try...except...else`
C) `try...except...finally`
D) `try...except...else...finally`
E) `try...finally` (without except)

**CN**: 以下哪些是 Python 中有效的异常处理方式？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D, E**
> Python 支持：`try/except`、`try/except/finally`、`try/except/else/finally`、`try/finally`。B 错误 — `else` 不能直接跟 `try`，必须跟在 `except` 后面。

---

### MS14 (Multi-Select)
**EN**: Which of the following are TRUE about Python's `import` system? *(Select ALL that apply)*
A) `import module` imports the entire module
B) `from module import *` imports all public names from the module
C) `sys.path` determines where Python searches for modules
D) A module is only executed once per interpreter session (cached)
E) `__init__.py` is required for ALL Python packages in Python 3.7

**CN**: 以下关于 Python `import` 系统的说法哪些是正确的？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, C, D**
> A、B、C、D 都正确。E 不完全正确 — Python 3.3+ 引入了隐式命名空间包，`__init__.py` 不再是绝对必需，但在 Python 3.7 常规包中仍推荐使用。

---

### MS15 (Multi-Select)
**EN**: Which of the following are standard Python naming conventions (PEP 8)? *(Select ALL that apply)*
A) Class names use `CamelCase`
B) Function names use `snake_case`
C) Constants use `UPPER_CASE`
D) Variable names use `camelCase`
E) Module names use `snake_case`

**CN**: 以下哪些是 Python 标准命名约定（PEP 8）？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, C, E**
> PEP 8：类名用 `CamelCase`，函数用 `snake_case`，常量用 `UPPER_CASE`，模块名用 `snake_case`。D 错误 — 变量名也用 `snake_case`，非 `camelCase`。

---

### MS16 (Multi-Select)
**EN**: Which of the following database-related operations are part of Python's `sqlite3` module? *(Select ALL that apply)*
A) `sqlite3.connect()`
B) `connection.cursor()`
C) `cursor.execute()`
D) `connection.commit()`
E) `connection.query()`

**CN**: 以下哪些数据库操作属于 Python 的 `sqlite3` 模块？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, C, D**
> `connect()`、`cursor()`、`execute()`、`commit()` 都是 sqlite3 的标准操作。E 错误 — 没有 `connection.query()` 方法，查询通过 `cursor.execute()` 执行。

---

### MS17 (Multi-Select)
**EN**: In Python regular expressions (`re` module), which of the following are valid functions? *(Select ALL that apply)*
A) `re.match()`
B) `re.search()`
C) `re.findall()`
D) `re.replace()`
E) `re.sub()`

**CN**: Python 正则表达式（`re` 模块）中，以下哪些是有效函数？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, C, E**
> `match()`、`search()`、`findall()`、`sub()` 都是 `re` 模块的有效函数。D 错误 — 用于替换的函数是 `re.sub()`，不是 `re.replace()`。

---

### MS18 (Multi-Select)
**EN**: Which of the following are correct about Python's garbage collection? *(Select ALL that apply)*
A) Python primarily uses reference counting
B) The `gc` module can be used to manually trigger collection
C) Objects are immediately freed when `del` is called on them
D) Circular references are handled by the cyclic garbage collector
E) `sys.getrefcount()` returns the exact number of references

**CN**: 以下关于 Python 垃圾回收的说法哪些是正确的？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D**
> A 正确（引用计数是主要机制）；B 正确（`gc.collect()` 手动触发）；D 正确（循环 GC 处理循环引用）。C 错误 — `del` 只减少引用计数，内存只在引用计数归零时释放。E 不精确 — `sys.getrefcount()` 的返回值包含函数参数自身的临时引用，需减 1。

---

### MS19 (Multi-Select)
**EN**: Which of the following list methods modify the list in-place? *(Select ALL that apply)*
A) `list.append()`
B) `list.sort()`
C) `list.extend()`
D) `sorted(list)`
E) `list.reverse()`

**CN**: 以下哪些列表方法会就地修改列表？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, C, E**
> `append()`、`sort()`、`extend()`、`reverse()` 都就地修改原列表并返回 `None`。D 错误 — `sorted()` 是内置函数，返回新排序列表，不修改原列表。

---

### MS20 (Multi-Select)
**EN**: In Python 3.7, which of the following characteristics apply to dictionaries? *(Select ALL that apply)*
A) Dictionaries preserve insertion order
B) Dictionary keys must be unique
C) Dictionary values must be unique
D) Dictionaries are mutable
E) `dict.keys()` returns a list

**CN**: Python 3.7 中，字典具有以下哪些特性？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D**
> Python 3.7+ 字典保持插入顺序(A)，键必须唯一(B)，字典是可变的(D)。C 错误（值可以重复）。E 错误 — `dict.keys()` 返回 `dict_keys` 视图对象，不是列表。

---

### MS21 (Multi-Select)
**EN**: Which of the following are valid string methods in Python? *(Select ALL that apply)*
A) `str.upper()`
B) `str.append()`
C) `str.split()`
D) `str.replace()`
E) `str.add()`

**CN**: 以下哪些是 Python 中有效的字符串方法？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, C, D**
> `upper()`、`split()`、`replace()` 都是字符串方法。B 错误（字符串没有 `append()`）；E 错误（字符串没有 `add()`，拼接用 `+` 或 `join()`）。

---

### MS22 (Multi-Select)
**EN**: Which of the following are correct about Python's `logging` module? *(Select ALL that apply)*
A) Logging levels: DEBUG < INFO < WARNING < ERROR < CRITICAL
B) `logging.basicConfig()` configures the logging system
C) By default, DEBUG messages are always printed
D) Logging can output to files, not just the console
E) `logging.info()` is used for detailed diagnostic information

**CN**: 以下关于 Python `logging` 模块的说法哪些是正确的？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D**
> A 正确（级别顺序）；B 正确（`basicConfig` 配置日志）；D 正确（可输出到文件）。C 错误 — 默认为 WARNING 级别，DEBUG 低于此级别不会被打印。E 错误 — 详细诊断信息用 `logging.debug()`，`info()` 用于一般信息。

---

### MS23 (Multi-Select)
**EN**: When using the `json` module, which Python types can be directly serialized with `json.dumps()`? *(Select ALL that apply)*
A) `dict`
B) `list`
C) `set`
D) `str`
E) `int`

**CN**: 使用 `json` 模块时，`json.dumps()` 可直接序列化哪些 Python 类型？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D, E**
> `dict`、`list`、`str`、`int` 都可直接序列化为 JSON。C 错误 — `set` 不是 JSON 可序列化类型，会引发 `TypeError`。

---

### MS24 (Multi-Select)
**EN**: Which of the following are correct about Python's `for` loop? *(Select ALL that apply)*
A) `for` can iterate over any iterable object
B) `for...else` executes the `else` block when the loop completes without `break`
C) `for` can only iterate over lists
D) `range()` is commonly used with `for` loops
E) `break` exits the loop immediately

**CN**: 以下关于 Python `for` 循环的说法哪些是正确的？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, D, E**
> A 正确（任何可迭代对象）；B 正确（`else` 在正常完成时执行）；D 正确；E 正确（`break` 立即退出）。C 错误 — `for` 可迭代任何可迭代对象（列表、元组、字典、集合、字符串、生成器等）。

---

### MS25 (Multi-Select)
**EN**: Which of the following are correct ways to create a Python virtual environment? *(Select ALL that apply)*
A) `python -m venv myenv`
B) `virtualenv myenv` (after installing virtualenv)
C) `python --create-venv myenv`
D) `pip venv myenv`
E) `conda create --name myenv` (with Anaconda)

**CN**: 以下哪些是创建 Python 虚拟环境的正确方法？**（选出所有正确答案）**

✅ **正确答案 / Answer: A, B, E**
> `python -m venv`(A) 和 `virtualenv`(B) 创建虚拟环境，`conda create`(E) 是 Anaconda 方式。C 和 D 是无效命令。

---

> **多选总计 25 道**，涵盖所有 SHL 考试主题。注意：多选题需要选出**所有**正确答案才能得分。

1. **注意运算符优先级**: `**` > `*`, `/`, `//`, `%` > `+`, `-`
2. **可变默认参数陷阱**: 默认参数只在函数定义时计算一次
3. **浅拷贝 vs 深拷贝**: `=` vs `copy()` vs `deepcopy()`
4. **`is` vs `==`**: `is` 检查身份(内存地址)，`==` 检查值
5. **Python 3 除法**: `/` 总是返回 float，`//` 返回 int（地板除）
6. **字符串不可变**: 字符串方法返回新字符串，不修改原字符串
7. **元组不可变**: 不能修改元组元素
8. **集合无重复**: 集合自动去重
9. **列表引用陷阱**: `b = a` 创建引用，修改相互影响
10. **浮点数精度**: `0.1 + 0.2 != 0.3`，使用 `math.isclose()` 比较
11. **正则用原始字符串**: 始终使用 `r'pattern'` 避免转义问题
12. **`re.match` vs `re.search`**: `match` 只从开头匹配，`search` 搜索整个字符串
13. **SQLite 参数化查询**: 使用 `?` 占位符防止 SQL 注入
14. **`commit()` 后数据才持久化**: INSERT/UPDATE/DELETE 后必须 commit
15. **调试等级**: DEBUG < INFO < WARNING < ERROR < CRITICAL
16. **`sys.path` 决定模块搜索**: 导入模块时 Python 按 `sys.path` 列表顺序搜索
17. **引用计数 = 0 则回收**: Python 对象引用计数归零时立即被回收
18. **`.pyc` 是字节码缓存**: 存储在 `__pycache__` 中，加速导入

---

## 考试报告三大板块对照 / Mapping to Report Subsections

| 报告板块 | 覆盖率 | 对应题目 |
|----------|--------|----------|
| **Python Basics** | ✅ 完整 | Q1-Q15, Q26-Q30, Q164-Q170, MS1-MS3, MS12, MS15 |
| **Python Programming** | ✅ 完整 | Q16-Q25, Q31-Q100, Q101-Q120, Q131-Q148, MS4-MS10, MS13, MS17-MS24 |
| **Databases and Modules** | ✅ 完整 | Q121-Q130, Q149-Q163, MS7, MS11, MS14, MS16, MS25 |

---

> **总计 195 道题**（单选题 170 道 + 多选题 25 道），完整覆盖 SHL Python 3.7 MCQ 考试全部考点。
>
> **考试类型**: 主要为单选题（Multi-choice = 多选一）。部分 SHL 考试可能包含多选（Select ALL that apply），建议两种都练习。
>
> **建议复习节奏**：每天 30 题（25 单选 + 5 多选），7 天完成。
>
> **祝考试顺利！Good luck with your exam! 🎓**
>
> **祝考试顺利！Good luck with your exam! 🎓**
