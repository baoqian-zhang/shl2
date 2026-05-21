# SHL Python 3.7 MCQ 考试题库（第二套 / Set 2）

> **考试信息**: Python 3.7 | Multi-choice test | Python Programming + Databases + Modules
> **说明**: 本题库为**第二套全新题目**，与第一套完全不重复。每道题含英文原题、中文翻译、准确答案和详细解析。
> **所有答案已经过严格验证，确保准确无误。**

---

## Set 2 — 题型分布 / Topic Coverage

| 章节 | 内容 | 题号 |
|------|------|------|
| S2-1 | Python 基础 / Basics | Q1-Q10 |
| S2-2 | 程序结构与执行 / Program Structure | Q11-Q16 |
| S2-3 | 内存管理 / Memory Management | Q17-Q22 |
| S2-4 | 运算符与类型 / Operators & Types | Q23-Q32 |
| S2-5 | 字符串处理 / String Handling | Q33-Q42 |
| S2-6 | 序列与文件操作 / Sequences & Files | Q43-Q56 |
| S2-7 | 函数与作用域 / Functions & Scope | Q57-Q70 |
| S2-8 | 排序与Lambda / Sorting & Lambda | Q71-Q76 |
| S2-9 | 错误与异常处理 / Errors & Exceptions | Q77-Q84 |
| S2-10 | 正则表达式 / Regular Expressions | Q85-Q92 |
| S2-11 | 面向对象编程 / OOP | Q93-Q102 |
| S2-12 | 模块与包 / Modules & Packages | Q103-Q110 |
| S2-13 | 标准库 / Standard Library | Q111-Q122 |
| S2-14 | 调试与测试 / Debugging | Q123-Q128 |
| S2-15 | 数据库 / Databases | Q129-Q136 |
| S2-16 | 网络与项目 / Networking & Project | Q137-Q142 |

---

## S2-1: Python 基础 / Python Basics

---

### S2Q1
**EN**: Which of the following is NOT a valid way to start a comment in Python?
A) `# This is a comment`
B) `""" This is a docstring """`
C) `// This is a comment`
D) `''' Multi-line comment '''`

**CN**: 以下哪个不是 Python 中有效的注释写法？

✅ **正确答案 / Answer: C**
> Python 使用 `#` 表示单行注释。`""" """` 和 `''' '''` 是多行字符串，常用作文档字符串(docstring)。`//` 是 C/Java 的注释语法，Python 不支持。

---

### S2Q2
**EN**: What is the output?
```python
x = 7
y = 2
print(x / y)
```
A) 3
B) 3.0
C) 3.5
D) 3.50

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> Python 3 中 `/` 运算符总是返回 float 类型。`7 / 2 = 3.5`。

---

### S2Q3
**EN**: In Python, `pass` statement is used to:
A) Skip the current iteration of a loop
B) Do nothing — acts as a placeholder
C) Exit a function
D) Raise an exception

**CN**: Python 中 `pass` 语句用于什么？

✅ **正确答案 / Answer: B**
> `pass` 是空操作语句，用作占位符。在需要语法上必须有语句但代码不需要执行任何操作的地方使用（如空函数体、空类定义）。

---

### S2Q4
**EN**: What is the output?
```python
print(type(True))
```
A) `<class 'bool'>`
B) `<class 'int'>`
C) `<class 'str'>`
D) `<class 'True'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `True` 和 `False` 在 Python 中是 `bool` 类型。注意 `bool` 是 `int` 的子类，但 `type(True)` 返回 `<class 'bool'>`。

---

### S2Q5
**EN**: What is the output?
```python
print(print("Hello"))
```
A) `Hello`
B) `Hello` then `None`
C) `None`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 第一行先执行内层 `print("Hello")` 输出"Hello"，然后 `print()` 函数返回 `None`，外层 `print(None)` 输出 `None`。所以先输出 `Hello` 换行后输出 `None`。

---

### S2Q6
**EN**: Which of the following variable names is invalid in Python?
A) `myVar`
B) `_count`
C) `1st_value`
D) `__private`

**CN**: 以下哪个变量名在 Python 中无效？

✅ **正确答案 / Answer: C**
> Python 变量名不能以数字开头。`1st_value` 以数字 1 开头，无效。其他选项都符合命名规则。

---

### S2Q7
**EN**: What is the output?
```python
a, b = 10, 20
a, b = b, a + b
print(a, b)
```
A) `10 20`
B) `20 30`
C) `20 10`
D) `10 10`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 先计算右侧全部表达式再赋值。右侧 = (20, 10+20) = (20, 30)，然后赋值给 `a=20, b=30`。

---

### S2Q8
**EN**: What does the `isinstance()` function do?
A) Checks if two objects are the same type
B) Checks if an object is an instance of a specified class (or its subclass)
C) Checks if an object exists in memory
D) Checks if a variable has been defined

**CN**: `isinstance()` 函数的作用是什么？

✅ **正确答案 / Answer: B**
> `isinstance(obj, class)` 检查 obj 是否是指定类（或其子类）的实例。例如 `isinstance(5, int)` 返回 `True`。注意：`isinstance` 会考虑继承关系，而 `type(obj) == class` 不会。

---

### S2Q9
**EN**: What is the output?
```python
value = input("Enter: ")
# User types: 42
print(type(value))
```
A) `<class 'int'>`
B) `<class 'float'>`
C) `<class 'str'>`
D) `<class 'NoneType'>`

**CN**: 以下代码的输出是什么？（用户输入 42）

✅ **正确答案 / Answer: C**
> `input()` 始终返回字符串。即使用户输入的是数字，返回的也是 `"42"`（字符串）。需要手动转换为 `int()` 或 `float()`。

---

### S2Q10
**EN**: What is the output?
```python
x = 0
if x:
    print("A")
elif not x:
    print("B")
else:
    print("C")
```
A) A
B) B
C) C
D) A B

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `x = 0` 在布尔上下文中为 `False`，`if x:` 不成立。`not x` 为 `True`，所以执行 `elif` 块输出 "B"。`else` 分支永不执行。

---

## S2-2: 程序结构与执行 / Program Structure & Execution

---

### S2Q11
**EN**: What is the output when the following script is executed?
```python
# mymodule.py
def greet():
    return "Hi"

print(__name__)
```
A) `__main__`
B) `mymodule`
C) `Hi`
D) `None`

**CN**: 以下脚本执行时的输出是什么？

✅ **正确答案 / Answer: A**
> 当 `.py` 文件被直接执行时，全局变量 `__name__` 被设为 `"__main__"`。如果被 `import`，则为模块名。

---

### S2Q12
**EN**: What does the `__pycache__` directory contain?
A) Python source code
B) Compiled bytecode (.pyc files) for faster imports
C) Configuration files
D) Temporary data files

**CN**: `__pycache__` 目录包含什么？

✅ **正确答案 / Answer: B**
> `__pycache__` 目录包含 `.pyc` 编译字节码文件。当模块被导入时，Python 将源码编译为字节码并缓存到此目录，下次导入时直接加载字节码加快速度。

---

### S2Q13
**EN**: What is the output?
```python
if True:
    print("A")
print("B")
```
A) A
B) B
C) A B (on separate lines)
D) AB

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `if True:` 为真执行 `print("A")` 输出 "A"，然后 `print("B")` 输出 "B"。由于 `print()` 默认添加换行符，输出在单独行上。

---

### S2Q14
**EN**: Which line will cause a syntax error?
```python
# 1
if True:
    print("A")
   print("B")
# 2
```
A) Line 1
B) Line 2
C) Line 3
D) No error

**CN**: 哪一行会引发语法错误？

✅ **正确答案 / Answer: C**
> 同一代码块必须保持相同的缩进级别。`print("A")` 缩进 4 个空格，`print("B")` 缩进 3 个空格，缩进不一致引发 `IndentationError`。

---

### S2Q15
**EN**: What is the output?
```python
for i in range(1, 4):
    if i == 2:
        pass
    else:
        print(i, end=" ")
```
A) 1 2 3
B) 1 3
C) 3
D) 1 2

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> i=1 → 输出 1；i=2 → `pass` 什么都不做；i=3 → 输出 3。结果为 "1 3"。

---

### S2Q16
**EN**: What is the output?
```python
result = 0
for num in range(1, 5):
    if num == 3:
        continue
    result += num
print(result)
```
A) 10
B) 7
C) 6
D) 3

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `range(1, 5)` 生成 1, 2, 3, 4。当 num=3 时 `continue` 跳过。累加：1+2+4 = 7。

---

## S2-3: 内存管理 / Memory Management

---

### S2Q17
**EN**: What is the output?
```python
a = [1, 2, 3]
b = a
c = a[:]
a.append(4)
print(len(b), len(c))
```
A) `3 3`
B) `4 3`
C) `4 4`
D) `3 4`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `b = a` 创建引用（指向同一列表），`c = a[:]` 创建浅拷贝（新列表）。`a.append(4)` 后 a 和 b 长度变为 4，c 仍是 3。

---

### S2Q18
**EN**: What is the output?
```python
x = 10
y = x
x = 20
print(y)
```
A) 10
B) 20
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 整数是不可变类型。`y = x` 后 y 指向值 10，`x = 20` 创建新对象 20 并让 x 指向它，y 仍指向 10。与列表等可变类型行为不同。

---

### S2Q19
**EN**: What is the output?
```python
import gc
print(gc.isenabled())
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 默认情况下，Python 的垃圾回收器是启用的。`gc.isenabled()` 返回 `True`。可以通过 `gc.disable()` 禁用。

---

### S2Q20
**EN**: What happens when a function ends and its local variable was the only reference to an object?
A) The object is destroyed immediately by `del`
B) The object's reference count decreases; if it reaches 0, the memory is freed
C) The object remains in memory until program exit
D) The object is moved to a special cache

**CN**: 当函数结束时，其局部变量是对某个对象的唯一引用，会发生什么？

✅ **正确答案 / Answer: B**
> 函数结束时局部变量超出作用域，对象的引用计数减 1。如果引用计数变为 0，Python 立即回收该对象的内存。

---

### S2Q21
**EN**: Which of the following can cause a circular reference in Python?
A) `a = 5; b = a`
B) `a = []; a.append(a)`
C) `a = (1, 2)`
D) `a = "Hello"; b = "Hello"`

**CN**: 以下哪个会导致 Python 中的循环引用？

✅ **正确答案 / Answer: B**
> `a.append(a)` 使列表 a 包含对自身的引用（a[0] 是 a 本身），形成循环引用。循环引用使得引用计数永远不会归零，依赖垃圾回收器检测处理。

---

### S2Q22
**EN**: What is the output?
```python
x = [1, 2, 3]
y = [1, 2, 3]
print(id(x) == id(y))
x[0] = 99
print(x is y)
```
A) True 换行 True
B) False 换行 False
C) True 换行 False
D) False 换行 True

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `x` 和 `y` 是两个不同的列表对象（内容相同但身份不同），`id(x) != id(y)`，所以 `id(x) == id(y)` 为 `False`。`x is y` 也为 `False`。修改 x 不影响 y。

---

## S2-4: 运算符与类型 / Operators & Types

---

### S2Q23
**EN**: What is the output?
```python
print(not 5 > 3)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `5 > 3` 为 `True`，`not True` 为 `False`。运算符优先级：比较 (`>`) 高于逻辑非 (`not`)。

---

### S2Q24
**EN**: What is the output?
```python
x = 10
x += 5 * 2
print(x)
```
A) 20
B) 30
C) 100
D) 17

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `x += 5 * 2` 等价于 `x = x + (5 * 2)`。先计算 `5 * 2 = 10`，然后 `10 + 10 = 20`。

---

### S2Q25
**EN**: What is the output?
```python
print(2 < 3 and 3 < 4 < 5)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `2 < 3` 为 `True`，`3 < 4 < 5` 等价于 `(3 < 4) and (4 < 5)` 也为 `True`。`True and True` = `True`。

---

### S2Q26
**EN**: What is the output?
```python
print(0 or 5 and 3)
```
A) 0
B) 5
C) 3
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 优先级：`and` 高于 `or`。先计算 `5 and 3`：`5` 为真，返回第二个操作数 3。然后 `0 or 3`：`0` 为假，返回第二个操作数 3。

---

### S2Q27
**EN**: What is the output?
```python
print(3 * "ab" + "c")
```
A) `"abc"` 重复 3 次
B) `"ababc"`
C) `"abababc"`
D) `"3abc"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `3 * "ab"` = `"ababab"`，然后 `+ "c"` = `"abababc"`。运算符优先级：`*` 高于 `+`。

---

### S2Q28
**EN**: What is the output?
```python
print(type(10.0 // 3))
```
A) `<class 'float'>`
B) `<class 'int'>`
C) `<class 'double'>`
D) `<class 'long'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> Python 3 中 `//` 的结果类型取决于操作数的类型。`10.0` 是 float，所以 `10.0 // 3` 返回 `3.0`（float 类型）。如果两个操作数都是 int，结果是 int。

---

### S2Q29
**EN**: What is the output?
```python
x = 1
y = 2
z = 3
print(x == y < z)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> Python 链式比较：`x == y < z` 等价于 `(x == y) and (y < z)`。`1 == 2` 为 `False`，短路求值返回 `False`。

---

### S2Q30
**EN**: What is the output?
```python
print(~5)
```
A) -5
B) -6
C) 4
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `~` 是按位取反运算符。`~x = -(x+1)`。`~5 = -(5+1) = -6`。二进制表示：5 是 `0101`，取反得 `1010`（补码表示 = -6）。

---

### S2Q31
**EN**: What is the output?
```python
x = 6
x ^= 3
print(x)
```
A) 3
B) 5
C) 6
D) 9

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `^` 是按位异或(XOR)。`x ^= 3` 等价于 `x = x ^ 3`。6(110) XOR 3(011) = 5(101)。

---

### S2Q32
**EN**: What is the output?
```python
x = 8
x >>= 2
print(x)
```
A) 2
B) 4
C) 16
D) 0

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `>>=` 是右移位赋值。`x >>= 2` 等价于 `x = x >> 2`。8(1000) 右移 2 位 = 2(0010)。

---

## S2-5: 字符串处理 / String Handling

---

### S2Q33
**EN**: What is the output?
```python
s = "Hello"
print(s.ljust(10, '*'))
```
A) `"Hello*****"`
B) `"*****Hello"`
C) `"Hello*"`
D) `"*Hello*"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `ljust(width, fillchar)` 左对齐字符串，右侧用指定字符填充到指定宽度。"Hello" 5 个字符，填充到 10 个，右侧加 5 个 `*`。

---

### S2Q34
**EN**: What is the output?
```python
print("   Hello   ".strip())
```
A) `"   Hello   "`
B) `"Hello"`
C) `"Hello   "`
D) `"   Hello"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `strip()` 去除字符串首尾的空白字符（空格、制表符、换行符）。结果 `"Hello"`。

---

### S2Q35
**EN**: What is the output?
```python
text = "Python programming"
print(text.find("pro"))
```
A) 0
B) 7
C) 8
D) -1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `find("pro")` 返回子串 `"pro"` 首次出现的索引。"Python programming" 中 "pro" 从索引 7 开始（P-y-t-h-o-n-空格-p-r-o...）。

---

### S2Q36
**EN**: What is the output?
```python
text = "a,b,c,d"
print(text.split(",", 2))
```
A) `['a', 'b', 'c,d']`
B) `['a', 'b', 'c', 'd']`
C) `['a,b', 'c,d']`
D) `['a', 'b,c,d']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `split(",", 2)` 最多分 2 次。第一次在第一个逗号处分，第二次在第二个逗号处分，剩余部分 `"c,d"` 作为最后一个元素。结果 `['a', 'b', 'c,d']`。

---

### S2Q37
**EN**: What is the output?
```python
print("abcdefg".startswith(("ab", "bc")))
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `startswith()` 可以接受元组作为参数，检查字符串是否以任意一个前缀开头。`"abcdefg"` 以 `"ab"` 开头，返回 `True`。

---

### S2Q38
**EN**: What is the output?
```python
s = "python"
print(s.capitalize())
```
A) `"Python"`
B) `"PYTHON"`
C) `"python"`
D) `"P"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `capitalize()` 将字符串的首字母大写，其余字母小写。`"python"` → `"Python"`。

---

### S2Q39
**EN**: What is the output?
```python
s = "123"
print(s.zfill(5))
```
A) `"00123"`
B) `"12300"`
C) `"  123"`
D) `"00000"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `zfill(width)` 在字符串左侧填充零到指定宽度。"123" 3 个字符，填充到 5 个，左侧加两个 0 → `"00123"`。

---

### S2Q40
**EN**: What is the output?
```python
print("Python".isalpha())
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `isalpha()` 检查字符串是否只包含字母字符。"Python" 只包含字母，返回 `True`。

---

### S2Q41
**EN**: What is the output?
```python
s = "Hello World"
print(s.swapcase())
```
A) `"HELLO WORLD"`
B) `"hELLO wORLD"`
C) `"hello world"`
D) `"Hello World"`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `swapcase()` 将大写字母转为小写，小写字母转为大写。"Hello World" → "hELLO wORLD"。

---

### S2Q42
**EN**: What is the output?
```python
s = "file.txt"
print(s.endswith((".txt", ".md")))
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `endswith()` 也可以接受元组参数。`"file.txt"` 以 `".txt"` 结尾，返回 `True`。

---

## S2-6: 序列与文件操作 / Sequences & File Operations

---

### S2Q43
**EN**: What is the output?
```python
lst = [10, 20, 30, 40, 50]
print(lst[-2])
```
A) 30
B) 40
C) 50
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 负索引 -1 表示最后一个元素，-2 表示倒数第二个。`lst[-2]` = 40。

---

### S2Q44
**EN**: What is the output?
```python
lst = [1, 2, 3, 4]
del lst[1]
print(lst)
```
A) `[1, 3, 4]`
B) `[2, 3, 4]`
C) `[1, 2, 3, 4]`
D) `[1, 2, 3]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `del lst[1]` 删除索引 1 的元素（值为 2）。列表变为 `[1, 3, 4]`。

---

### S2Q45
**EN**: What is the output?
```python
lst = [5, 3, 1, 4, 2]
new = sorted(lst)
print(lst[0], new[0])
```
A) `5 1`
B) `1 1`
C) `5 5`
D) `1 5`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `sorted(lst)` 返回新的排序列表，不修改原列表。`lst` 仍是 `[5, 3, 1, 4, 2]`，`lst[0]` = 5。`new` = `[1, 2, 3, 4, 5]`，`new[0]` = 1。

---

### S2Q46
**EN**: What is the output?
```python
t = (1, 2, 3)
print(t + (4, 5))
```
A) `(1, 2, 3, 4, 5)`
B) `(1, 2, 3, (4, 5))`
C) Error
D) `(5, 4, 3, 2, 1)`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `+` 运算符连接两个元组，生成新元组。`(1, 2, 3) + (4, 5)` = `(1, 2, 3, 4, 5)`。

---

### S2Q47
**EN**: What is the output?
```python
s1 = {1, 2, 3}
s2 = {3, 4, 5}
print(s1 - s2)
```
A) `{1, 2, 3, 4, 5}`
B) `{1, 2}`
C) `{3}`
D) `{4, 5}`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `-` 是集合差集运算符。`s1 - s2` 返回在 s1 中但不在 s2 中的元素：`{1, 2}`。

---

### S2Q48
**EN**: What is the output?
```python
d = {x: x**2 for x in range(1, 5)}
print(d[3])
```
A) 9
B) 16
C) 6
D) 12

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 字典推导式生成 `{1:1, 2:4, 3:9, 4:16}`。`d[3]` = 3² = 9。

---

### S2Q49
**EN**: What is the output?
```python
d = {"apple": 5, "banana": 3}
print("orange" in d)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `in` 运算符检查键(key)是否在字典中。"orange" 不是字典中的键，返回 `False`。

---

### S2Q50
**EN**: What is the output?
```python
lst = [1, 2, 3]
lst.insert(1, 99)
print(lst)
```
A) `[1, 99, 2, 3]`
B) `[99, 1, 2, 3]`
C) `[1, 2, 99, 3]`
D) `[1, 2, 3, 99]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `insert(index, value)` 在指定索引位置插入元素。`insert(1, 99)` 在索引 1 处插入 99，原元素右移。结果 `[1, 99, 2, 3]`。

---

### S2Q51
**EN**: What is the output?
```python
a = [10, 20, 30]
b = [40, 50]
print(a + b)
```
A) `[10, 20, 30, 40, 50]`
B) `[[10, 20, 30], [40, 50]]`
C) `[50, 40, 30, 20, 10]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `+` 运算符连接两个列表（不修改原列表）。`a + b` = `[10, 20, 30, 40, 50]`。

---

### S2Q52
**EN**: What is the output?
```python
s = {1, 2, 3}
s.discard(2)
s.discard(10)
print(len(s))
```
A) 1
B) 2
C) 3
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `discard()` 移除指定元素，如果元素不存在也不会报错（不同于 `remove()` 会引发 `KeyError`）。先移除 2，集合变为 `{1, 3}`，discard(10) 不报错。`len(s)` = 2。

---

### S2Q53
**EN**: What is the output?
```python
t = (10, 20, 30)
print(t.index(20))
```
A) 0
B) 1
C) 2
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `index(value)` 返回指定值首次出现的索引。20 在元组索引 1 处。

---

### S2Q54
**EN**: What is the output?
```python
with open("data.txt", "w") as f:
    print("Hello", file=f)
```
A) Writes "Hello" followed by a newline to data.txt
B) Writes "Hello" without newline to data.txt
C) Writes the string representation of f to data.txt
D) Error

**CN**: 以下代码的作用是什么？

✅ **正确答案 / Answer: A**
> `print()` 的 `file` 参数指定输出目标文件。`print("Hello", file=f)` 将 "Hello" 写入文件并自动添加换行符（默认 `end="\n"`）。

---

### S2Q55
**EN**: Which mode is used to open a file for reading and writing without truncating it?
A) `"rw"`
B) `"r+"`
C) `"rw+"`
D) `"wr"`

**CN**: 哪个模式用于以读写方式打开文件且不截断？

✅ **正确答案 / Answer: B**
> `"r+"` 表示读写模式，文件必须已存在，不会截断文件。`"w+"` 也会截断文件。

---

### S2Q56
**EN**: What is the output?
```python
with open("test.txt", "w") as f:
    f.writelines(["line1\n", "line2\n"])

with open("test.txt", "r") as f:
    lines = f.readlines()
    print(len(lines))
```
(Assume file doesn't exist before code runs)
A) 1
B) 2
C) 3
D) 4

**CN**: 以下代码的输出是什么？（假设文件在运行前不存在）

✅ **正确答案 / Answer: B**
> `writelines()` 写入列表中的每一行（不会自动添加换行符，已在每个字符串末尾包含 `\n`）。`readlines()` 读取所有行到列表中。有 2 行，所以 `len(lines) = 2`。

---

## S2-7: 函数与作用域 / Functions & Scope

---

### S2Q57
**EN**: What is the output?
```python
def func(x, y=10, z=20):
    return x + y + z

print(func(1, z=5))
```
A) 16
B) 26
C) 6
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `func(x=1, z=5)` 使用默认值 y=10。1 + 10 + 5 = 16。关键字参数可以省略默认参数。

---

### S2Q58
**EN**: What is the output?
```python
def func(a, b, *args):
    return a + b + sum(args)

print(func(1, 2, 3, 4, 5))
```
A) 3
B) 15
C) 12
D) 6

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> a=1, b=2, args=(3, 4, 5)。1 + 2 + (3+4+5) = 1 + 2 + 12 = 15。

---

### S2Q59
**EN**: What is the output?
```python
def func(**kwargs):
    return list(kwargs.keys())

print(func(name="Alice", age=30))
```
A) `['name', 'age']`
B) `['Alice', 30]`
C) `{'name', 'age'}`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `**kwargs` 将关键字参数收集为字典。`keys()` 返回所有键的视图，转为列表后为 `['name', 'age']`。

---

### S2Q60
**EN**: What is the output?
```python
def func(lst=[]):
    lst.append(len(lst))
    return lst

print(func())
print(func())
```
A) `[0]` 换行 `[0]`
B) `[0]` 换行 `[0, 1]`
C) `[]` 换行 `[]`
D) `[0]` 换行 `[1]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 可变默认参数陷阱。第一次调用时空列表 `[]`，`len([])=0`，追加 0 → `[0]`。第二次调用时列表仍是 `[0]`，`len([0])=1`，追加 1 → `[0, 1]`。

---

### S2Q61
**EN**: What is the output?
```python
x = 99

def outer():
    x = 10
    def inner():
        nonlocal x
        x += 5
        return x
    return inner()

print(outer())
```
A) 15
B) 10
C) 104
D) 99

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `nonlocal x` 引用外层函数 `outer` 中的 `x=10`。`x += 5` 将其改为 15。不影响全局变量 `x=99`。

---

### S2Q62
**EN**: What is the output?
```python
def multiply_by(n):
    def multiplier(x):
        return x * n
    return multiplier

double = multiply_by(2)
triple = multiply_by(3)
print(double(10), triple(10))
```
A) 20 30
B) 10 10
C) 20 20
D) 30 20

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 闭包(closure)：`double` 是乘 2 的函数，`triple` 是乘 3 的函数。`double(10)=20`, `triple(10)=30`。

---

### S2Q63
**EN**: What is the output?
```python
def func(x):
    return x * 2

def apply(func, value):
    return func(value)

print(apply(func, "Hi"))
```
A) `"HiHi"`
B) `"Hi"`
C) `"HiHiHi"`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 函数作为参数传递（一等公民）。`apply(func, "Hi")` 调用 `func("Hi")`，返回 `"Hi" * 2 = "HiHi"`。

---

### S2Q64
**EN**: What is the output?
```python
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))
```
A) 15
B) 120
C) 25
D) 24

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 递归计算阶乘：5! = 5 × 4 × 3 × 2 × 1 = 120。

---

### S2Q65
**EN**: What is the output?
```python
def check(a, b):
    return a // b, a % b

q, r = check(17, 5)
print(q, r)
```
A) 3 2
B) 2 3
C) 3 4
D) 17 5

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 函数返回元组，解包赋值。17 // 5 = 3，17 % 5 = 2。`q=3, r=2`。

---

### S2Q66
**EN**: What is the output?
```python
values = [1, 2, 3, 4]
result = 0
for val in values:
    if val % 2 != 0:
        continue
    result += val
print(result)
```
A) 6
B) 4
C) 10
D) 9

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `continue` 跳过奇数。只累加偶数：2 + 4 = 6。

---

### S2Q67
**EN**: What is the output?
```python
def make_counter():
    count = [0]
    def counter():
        count[0] += 1
        return count[0]
    return counter

c = make_counter()
print(c(), c(), c())
```
A) 1 2 3
B) 1 1 1
C) 0 0 0
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 利用列表可变对象存储状态。每次调用 `c()` 增加并返回计数。1, 2, 3。

---

### S2Q68
**EN**: What is the output?
```python
def outer(x):
    def inner(y):
        return x + y
    return inner

add5 = outer(5)
print(add5(10))
```
A) 5
B) 10
C) 15
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 闭包：`outer(5)` 返回 `inner`，`inner` 捕获了 x=5。`add5(10)` 即 `inner(10)`，返回 5 + 10 = 15。

---

### S2Q69
**EN**: What is the output?
```python
def func():
    pass

print(func())
```
A) Error
B) None
C) True
D) 0

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 没有 `return` 语句的函数隐式返回 `None`。`func()` 执行 `pass` 后返回 `None`。

---

### S2Q70
**EN**: What is the output?
```python
def func(a, b, *args, c=10):
    return a + b + c

print(func(1, 2, 3, 4, c=5))
```
A) 8
B) 10
C) 12
D) 15

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> a=1, b=2, `3, 4` 被 `*args` 收集（忽略），c=5（关键字参数覆盖默认值 10）。1 + 2 + 5 = 8。

---

## S2-8: 排序与Lambda / Sorting & Lambda

---

### S2Q71
**EN**: What is the output?
```python
words = ["apple", "kiwi", "banana"]
words.sort(key=len)
print(words)
```
A) `['apple', 'kiwi', 'banana']`
B) `['kiwi', 'apple', 'banana']`
C) `['banana', 'apple', 'kiwi']`
D) `['apple', 'banana', 'kiwi']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `sort(key=len)` 按字符串长度排序。"kiwi"(4) < "apple"(5) < "banana"(6)。

---

### S2Q72
**EN**: What is the output?
```python
items = [("Alice", 25), ("Bob", 20), ("Charlie", 30)]
items.sort(key=lambda x: x[1])
print(items[-1][0])
```
A) Alice
B) Bob
C) Charlie
D) 30

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `key=lambda x: x[1]` 按元组的第二个元素（年龄）排序。排序后 `[("Bob",20), ("Alice",25), ("Charlie",30)]`。`items[-1][0]` = 最后一个元素的第一个元素 = "Charlie"。

---

### S2Q73
**EN**: What is the output?
```python
f = lambda a, b=5: a + b
print(f(3, 10))
```
A) 13
B) 8
C) 15
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> lambda 同样支持默认参数。`f(3, 10)` 中 a=3, b=10（覆盖默认值 5），3 + 10 = 13。

---

### S2Q74
**EN**: What is the output?
```python
data = ["cat", "dog", "bee", "elephant"]
result = sorted(data, key=lambda s: s[-1])
print(result)
```
A) `['cat', 'dog', 'bee', 'elephant']`
B) `['bee', 'dog', 'cat', 'elephant']`
C) `['dog', 'cat', 'elephant', 'bee']`
D) `['elephant', 'bee', 'dog', 'cat']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `key=lambda s: s[-1]` 按最后一个字母排序。'ca**t**'(t), 'do**g**'(g), 'be**e**'(e), 'elephan**t**'(t)。按字母序：e(101) < g(103) < t(116)。排序后：bee(e), dog(g), cat(t), elephant(t)。cat 和 elephant 在排序中保持原始相对顺序（稳定排序）。结果：`['bee', 'dog', 'cat', 'elephant']`。

---

### S2Q75
**EN**: What is the output?
```python
pairs = [(1, 'a'), (2, 'c'), (1, 'b')]
pairs.sort(key=lambda x: (x[0], x[1]))
print(pairs)
```
A) `[(1, 'a'), (1, 'b'), (2, 'c')]`
B) `[(1, 'b'), (1, 'a'), (2, 'c')]`
C) `[(2, 'c'), (1, 'a'), (1, 'b')]`
D) `[(1, 'a'), (2, 'c'), (1, 'b')]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `key=lambda x: (x[0], x[1])` 先按第一个元素排序，相同时按第二个元素排序。`(1,'a') < (1,'b') < (2,'c')`。

---

### S2Q76
**EN**: What is the output?
```python
add = lambda x, y: x ** y
print(add(2, 3))
```
A) 5
B) 6
C) 8
D) 9

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `lambda x, y: x ** y` 计算 x 的 y 次幂。`2 ** 3 = 8`。

---

## S2-9: 错误与异常处理 / Errors & Exception Handling

---

### S2Q77
**EN**: What is the output?
```python
try:
    x = 5 / 0
except ArithmeticError:
    print("Math error")
except ZeroDivisionError:
    print("Zero division")
```
A) Math error
B) Zero division
C) Both Math error and Zero division
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 异常处理按顺序匹配，`ArithmeticError` 是 `ZeroDivisionError` 的父类。由于 `except ArithmeticError` 在前，先匹配到。如果两个 `except` 调换顺序，则会输出 "Zero division"。

---

### S2Q78
**EN**: Which of the following is the base class for all built-in Python exceptions?
A) `Exception`
B) `BaseException`
C) `Error`
D) `RuntimeError`

**CN**: 以下哪个是所有 Python 内置异常的基类？

✅ **正确答案 / Answer: B**
> `BaseException` 是所有异常的基类。`Exception` 继承自 `BaseException`，是所有非系统退出异常（如 `ValueError`、`TypeError`）的基类。`KeyboardInterrupt` 和 `SystemExit` 继承自 `BaseException` 但不继承自 `Exception`。

---

### S2Q79
**EN**: What is the output?
```python
try:
    print("A")
    raise ValueError("Error X")
    print("B")
except ValueError:
    print("C")
finally:
    print("D")
```
A) A C D
B) A B C D
C) A B D
D) A D

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 打印 A，然后 `raise` 引发异常，跳过 `print("B")`。`except` 捕获异常打印 C。`finally` 始终执行打印 D。

---

### S2Q80
**EN**: What is the output?
```python
try:
    raise TypeError("Type error")
except ValueError:
    print("Value")
except:
    print("Generic")
```
A) Value
B) Generic
C) Type error
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `TypeError` 不匹配 `ValueError`，所以第一个 `except` 跳过。裸 `except:` 捕获所有异常，打印 "Generic"。注意：裸 `except` 一般不推荐，会捕获包括 `SystemExit` 在内的所有异常。

---

### S2Q81
**EN**: What is the output?
```python
class CustomError(Exception):
    pass

try:
    raise CustomError("Something went wrong")
except CustomError as e:
    print(type(e).__name__)
```
A) Exception
B) CustomError
C) Something went wrong
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 自定义异常类 `CustomError` 继承自 `Exception`。`type(e).__name__` 返回异常类名 "CustomError"。

---

### S2Q82
**EN**: What is the output?
```python
def divide(a, b):
    assert b != 0, "Division by zero!"
    return a / b

print(divide(10, 2))
```
A) 5.0
B) 5
C) AssertionError
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `b=2` 非零，`assert` 通过（不引发异常），`10 / 2 = 5.0`。

---

### S2Q83
**EN**: What is the output?
```python
x = "Hello"
try:
    print(x[10])
except (IndexError, TypeError) as e:
    print(type(e).__name__)
```
A) IndexError
B) TypeError
C) Hello
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `x[10]` 字符串长度为 5，索引 10 超出范围，引发 `IndexError`。一个 `except` 可以捕获多种异常类型。

---

### S2Q84
**EN**: What is the output?
```python
try:
    pass
except:
    print("Error")
else:
    print("Success")
finally:
    print("Done")
```
A) Success 换行 Done
B) Error
C) Done
D) 无输出

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `try` 块中 `pass` 没有异常，执行 `else` 块打印 "Success"，然后 `finally` 执行打印 "Done"。

---

## S2-10: 正则表达式 / Regular Expressions

---

### S2Q85
**EN**: What does the regex pattern `[^0-9]` match?
A) Any digit
B) Any character that is NOT a digit
C) Zero or more digits
D) The characters '0', '9', and '^'

**CN**: 正则模式 `[^0-9]` 匹配什么？

✅ **正确答案 / Answer: B**
> `[^...]` 在字符类中的 `^` 表示取反（NOT）。`[^0-9]` 匹配任何不是数字的字符。

---

### S2Q86
**EN**: What is the output?
```python
import re
text = "apple,banana,grape"
result = re.split(r",", text, maxsplit=1)
print(result)
```
A) `['apple', 'banana', 'grape']`
B) `['apple', 'banana,grape']`
C) `['apple', 'banana', 'grape', '']`
D) `['apple,banana,grape']`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `re.split(",", text, maxsplit=1)` 只分割 1 次。在第一个逗号处分隔，剩余部分 `"banana,grape"` 作为第二个元素。

---

### S2Q87
**EN**: What is the output?
```python
import re
text = "Hello 123 World 456"
result = re.findall(r"[A-Z][a-z]+", text)
print(result)
```
A) `["Hello", "World"]`
B) `["123", "456"]`
C) `["Hello", "World", "123", "456"]`
D) `["H", "W"]`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `[A-Z][a-z]+` 匹配一个大写字母开头后跟一个或多个小写字母。匹配 "Hello" 和 "World"。

---

### S2Q88
**EN**: What is the output?
```python
import re
m = re.search(r"(?P<area>\d{3})-(?P<num>\d{4})", "800-1234")
print(m.group("area"))
```
A) "800-1234"
B) "800"
C) "1234"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `(?P<name>...)` 是命名捕获组语法。`m.group("area")` 返回名为 "area" 的组匹配的内容 "800"。

---

### S2Q89
**EN**: What is the output?
```python
import re
result = re.fullmatch(r"\d{3}", "123")
print(bool(result))
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `fullmatch()` 要求模式匹配**整个字符串**。"123" 正好是 3 个数字，匹配成功，返回 match 对象，`bool()` 为 `True`。

---

### S2Q90
**EN**: What is the output?
```python
import re
text = "data@example.com"
result = re.sub(r"@.*", "@domain.com", text)
print(result)
```
A) "data@example.com"
B) "data@domain.com"
C) "@domain.com"
D) "example.com"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `@.*` 匹配 `@` 及其后面的所有字符（`@example.com`），替换为 `@domain.com`。结果 `"data@domain.com"`。

---

### S2Q91
**EN**: What is the output?
```python
import re
text = "abc123def"
result = re.search(r"(\d+)([a-z]+)", text)
if result:
    print(result.group(2))
```
A) "123"
B) "def"
C) "123def"
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `(\d+)` 捕获数字 "123"，`([a-z]+)` 捕获字母 "def"。`group(2)` 返回第二个捕获组 "def"。

---

### S2Q92
**EN**: Which flag makes a regex case-insensitive?
A) `re.IGNORECASE` or `re.I`
B) `re.MULTILINE` or `re.M`
C) `re.DOTALL` or `re.S`
D) `re.VERBOSE` or `re.X`

**CN**: 哪个标志使正则表达式不区分大小写？

✅ **正确答案 / Answer: A**
> `re.IGNORECASE`（简写 `re.I`）使匹配不区分大小写。`re.MULTILINE` 改变 `^` 和 `$` 的行为，`re.DOTALL` 使 `.` 匹配换行符。

---

## S2-11: 面向对象编程 / OOP

---

### S2Q93
**EN**: What is the output?
```python
class A:
    x = 1

class B(A):
    pass

class C(A):
    x = 3

class D(B, C):
    pass

print(D.mro()[0].__name__)
```
A) A
B) B
C) C
D) D

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: D**
> `D.mro()` 返回方法解析顺序(Method Resolution Order)。`mro()[0]` 是 D 本身。Python 3 使用 C3 线性化算法，D 的 MRO 为 D → B → C → A。

---

### S2Q94
**EN**: What is the output?
```python
class Person:
    def __init__(self, name):
        self._name = name

    @property
    def name(self):
        return self._name.upper()

p = Person("Alice")
print(p.name)
```
A) Alice
B) ALICE
C) alice
D) Error (cannot call property like a method)

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `@property` 使 `name()` 方法可以作为属性访问（无需括号）。`p.name` 调用 getter 返回 `"Alice".upper()` = "ALICE"。

---

### S2Q95
**EN**: What is the output?
```python
class Circle:
    pi = 3.14
    
    def __init__(self, radius):
        self.radius = radius
    
    @classmethod
    def from_diameter(cls, diameter):
        return cls(diameter / 2)

c = Circle.from_diameter(10)
print(c.radius)
```
A) 5.0
B) 10.0
C) 3.14
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `@classmethod` 接收类 `cls` 作为第一个参数。`from_diameter(10)` 创建一个 `Circle` 实例，半径为 10/2 = 5.0。

---

### S2Q96
**EN**: What is the output?
```python
class MyClass:
    def __init__(self, val):
        self.val = val
    
    def __add__(self, other):
        return self.val + other.val * 2

a = MyClass(10)
b = MyClass(5)
print(a + b)
```
A) 15
B) 20
C) 30
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `__add__` 重载 `+` 运算符。`a + b` 调用 `a.__add__(b)` = `10 + 5 * 2` = 10 + 10 = 20（注意运算符优先级：`*` 先于 `+`）。

---

### S2Q97
**EN**: What is the output?
```python
class Parent:
    def show(self):
        return "Parent"

class Child(Parent):
    def show(self):
        return super().show() + " + Child"

c = Child()
print(c.show())
```
A) "Parent"
B) "Child"
C) "Parent + Child"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `super().show()` 调用父类的 `show()` 方法返回 "Parent"，然后拼接 " + Child"。结果 "Parent + Child"。

---

### S2Q98
**EN**: What is the output?
```python
class Vehicle:
    kind = "vehicle"

class Car(Vehicle):
    kind = "car"

class Boat(Vehicle):
    pass

print(Car.kind, Boat.kind)
```
A) "car vehicle"
B) "car car"
C) "vehicle vehicle"
D) "vehicle car"

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `Car` 覆盖了类变量 `kind = "car"`。`Boat` 没有覆盖，继承自 `Vehicle` 的 `kind = "vehicle"`。

---

### S2Q99
**EN**: What is the output?
```python
class A:
    def __init__(self):
        self.result = self.get_value()
    
    def get_value(self):
        return 1

class B(A):
    def get_value(self):
        return 2

b = B()
print(b.result)
```
A) 1
B) 2
C) None
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 子类 `B` 的 `__init__` 调用继承自父类的 `__init__`，其中 `self.get_value()` 动态调用子类重写后的方法（多态），返回 2。

---

### S2Q100
**EN**: What is the output?
```python
class Counter:
    count = 0
    
    def __init__(self):
        self.count += 1
        Counter.count += 1

a = Counter()
b = Counter()
print(a.count, Counter.count)
```
A) 1 2
B) 2 2
C) 1 1
D) 2 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `self.count += 1` 是实例属性赋值（创建实例属性，覆盖类属性），每个实例的 `self.count` 增加 `0→1`。`Counter.count` 是类属性，每次实例化加 1，两次后为 2。

---

### S2Q101
**EN**: What is the output?
```python
class Base:
    __value = "private"

    def get_value(self):
        return self.__value

class Derived(Base):
    def show(self):
        return self.__value

obj = Derived()
print(obj.get_value())
```
A) "private"
B) Error
C) None
D) "private" 换行 Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> 名称改编(name mangling)：`__value` 在 `Base` 类中被改编为 `_Base__value`。`get_value()` 正常访问。但 `Derived` 类中的 `self.__value` 被改编为 `_Derived__value`，与 `_Base__value` 不同。

---

### S2Q102
**EN**: What does `isinstance` return for an object that is an instance of a subclass?
```python
class Animal: pass
class Dog(Animal): pass

d = Dog()
print(isinstance(d, Animal))
```
A) True
B) False
C) None
D) Error

**CN**: 对于子类的实例，`isinstance` 返回什么？

✅ **正确答案 / Answer: A**
> `isinstance()` 考虑继承关系。`Dog` 是 `Animal` 的子类，所以 `d` 也是 `Animal` 的实例，返回 `True`。`type(d) == Animal` 则返回 `False`（严格类型检查）。

---

## S2-12: 模块与包 / Modules & Packages

---

### S2Q103
**EN**: What is the output?
```python
import math as m
print(m.ceil(4.1))
```
A) 4
B) 5
C) 4.0
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `import math as m` 使用别名(as)导入。`m.ceil(4.1)` = `math.ceil(4.1)` = 5。

---

### S2Q104
**EN**: What is the output?
```python
import sys
print(hasattr(sys, 'version'))
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `hasattr(obj, name)` 检查对象是否具有指定属性。`sys` 模块有 `version` 属性，返回 `True`。

---

### S2Q105
**EN**: When a module is imported, what does `dir(module)` return?
A) A list of the module's file paths
B) A sorted list of attribute names in the module
C) The module's source code
D) The module's size

**CN**: 导入模块后，`dir(module)` 返回什么？

✅ **正确答案 / Answer: B**
> `dir(module)` 返回模块中定义的所有名称的排序列表（变量、函数、类等）。

---

### S2Q106
**EN**: What is the output?
```python
import math
print(math.sin.__module__)
```
A) "math"
B) "sin"
C) "__main__"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `__module__` 属性表示定义该函数/类的模块名。`math.sin` 在 `math` 模块中定义，所以 `sin.__module__` 为 `"math"`。

---

### S2Q107
**EN**: Which keyword must be used to make names from an import available in the current namespace?
A) `global`
B) `from`
C) `import`
D) `include`

**CN**: 必须使用哪个关键字使 import 的名称在当前命名空间中可用？

✅ **正确答案 / Answer: C**
> `import` 是必须的关键字。`from module import name` 和 `import module` 都使用 `import`。

---

### S2Q108
**EN**: What is the output?
```python
import sys
sys.path.insert(0, '/custom/path')
print('/custom/path' in sys.path)
```
A) True
B) False
C) Error
D) None

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `sys.path` 是一个普通列表，可以修改。`insert(0, path)` 将路径插入到搜索顺序的第一位。`in` 检查路径是否存在，返回 `True`。

---

### S2Q109
**EN**: What is the output?
```python
# Suppose we have a package structure:
# mypkg/__init__.py
# mypkg/mod.py containing: VAR = 42

import mypkg.mod
print(mypkg.mod.VAR)
```
A) 42
B) Error
C) "VAR"
D) None

**CN**: 以下代码的输出是什么？（假设 mypkg/mod.py 中有 VAR = 42）

✅ **正确答案 / Answer: A**
> `import mypkg.mod` 完整路径导入，通过 `mypkg.mod.VAR` 访问模块中的变量 42。

---

### S2Q110
**EN**: What does `__file__` represent in a Python module when it is imported?
A) The file name of the source code in text form
B) The absolute path to the module's .py or .pyc file
C) The module's documentation
D) The module's size in bytes

**CN**: 导入 Python 模块时，`__file__` 表示什么？

✅ **正确答案 / Answer: B**
> `__file__` 是模块文件路径（.py 或 .pyc 的绝对路径）。当文件被直接执行时，`__file__` 为脚本的路径。

---

## S2-13: 标准库 / Standard Library

---

### S2Q111
**EN**: What is the output?
```python
from datetime import timedelta
td = timedelta(days=1, hours=2)
print(td.total_seconds())
```
A) 86400
B) 7200
C) 93600
D) 3600

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> 1天 = 86400 秒，2小时 = 7200 秒。总计：86400 + 7200 = 93600 秒。

---

### S2Q112
**EN**: What is the output?
```python
from collections import OrderedDict
od = OrderedDict()
od['b'] = 2
od['a'] = 1
for k in od:
    print(k, end="")
```
A) ab
B) ba
C) Error
D) a b

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `OrderedDict` 保持键的插入顺序。先插入 'b' 后插入 'a'。输出 "ba"。

---

### S2Q113
**EN**: What is the output?
```python
import itertools
result = list(itertools.chain([1, 2], ['a', 'b']))
print(result)
```
A) `[1, 2, 'a', 'b']`
B) `[[1, 2], ['a', 'b']]`
C) `[1, 2]`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `itertools.chain()` 将多个可迭代对象连接成一个迭代器。`chain([1,2], ['a','b'])` 产生 1, 2, 'a', 'b'。

---

### S2Q114
**EN**: What is the output?
```python
from itertools import permutations
p = list(permutations('AB', 2))
print(len(p))
```
A) 1
B) 2
C) 4
D) 6

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `permutations('AB', 2)` 从 'A','B' 中选 2 个的所有排列：`('A','B')` 和 `('B','A')`。共 2 个。`P(2,2) = 2! = 2`。

---

### S2Q115
**EN**: What is the output?
```python
from itertools import combinations
c = list(combinations('ABC', 2))
print(len(c))
```
A) 2
B) 3
C) 6
D) 1

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `combinations('ABC', 2)` 从 'A','B','C' 中选 2 个的所有组合：AB, AC, BC。共 3 个。`C(3,2) = 3`。

---

### S2Q116
**EN**: What is the output?
```python
import os
path = os.path.join('a', 'b')
path2 = os.path.abspath(path)
print(os.path.isabs(path), os.path.isabs(path2))
```
A) True False
B) False True
C) True True
D) False False

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `os.path.join('a', 'b')` 返回相对路径 `'a/b'`（不是绝对路径）。`os.path.abspath()` 将其转换为绝对路径。`isabs('a/b')` = False，`isabs(绝对路径)` = True。

---

### S2Q117
**EN**: What is the output?
```python
import os
files = []
for entry in os.scandir('.'):
    if entry.is_file():
        files.append(entry.name)
print(type(files))
```
A) `<class 'generator'>`
B) `<class 'list'>`
C) `<class 'tuple'>`
D) `<class 'dict'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `files` 是一个列表（通过 `append()` 构建）。`os.scandir()` 返回迭代器，但最终 `files` 是 `list` 类型。

---

### S2Q118
**EN**: What is the output?
```python
import math
print(math.gcd(12, 18))
```
A) 3
B) 6
C) 12
D) 36

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `math.gcd(a, b)` 返回 a 和 b 的最大公约数。gcd(12, 18) = 6。

---

### S2Q119
**EN**: What is the output?
```python
import math
print(math.log(100, 10))
```
A) 1
B) 2
C) 10
D) 100

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `math.log(x, base)` 返回以 base 为底的对数。`log(100, 10) = log₁₀(100) = 2`。

---

### S2Q120
**EN**: What is the output?
```python
import json
data = [1, 2.5, "hello", True, None]
result = json.dumps(data)
print(result)
```
A) `'[1, 2.5, "hello", true, null]'`
B) `'[1, 2.5, "hello", True, None]'`
C) `'[1, 2.5, hello, true, null]'`
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `json.dumps()` 将 Python 对象序列化为 JSON 字符串。Python 的 `True` 转为 `true`，`None` 转为 `null`。带引号的字符串。

---

### S2Q121
**EN**: What is the output?
```python
from datetime import datetime
dt = datetime(2026, 5, 21, 14, 30, 0)
print(dt.hour)
```
A) 14
B) 5
C) 21
D) 30

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `datetime(year, month, day, hour, minute, second)` 创建时间对象。`.hour` 返回小时部分 14。

---

### S2Q122
**EN**: What is the output?
```python
import random
items = ['A', 'B', 'C', 'D']
result = random.sample(items, 2)
print(len(result))
```
A) 1
B) 2
C) 4
D) Depends on the random seed

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `random.sample(population, k)` 从总体中随机抽取 k 个唯一元素（不重复抽样），返回列表，长度始终为 k=2。

---

## S2-14: 调试与测试 / Debugging

---

### S2Q123
**EN**: What is the output?
```python
x = 5
assert x < 0, f"Expected negative, got {x}"
print("Done")
```
A) Done
B) AssertionError: Expected negative, got 5
C) Expected negative, got 5
D) Error: x is not negative

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `x=5` 不小于 0，`assert x < 0` 失败，引发 `AssertionError`，消息为 `"Expected negative, got 5"`。程序终止，`print("Done")` 不执行。

---

### S2Q124
**EN**: In the `logging` module, which method is used to create a named logger?
A) `logging.create(name)`
B) `logging.getLogger(name)`
C) `logging.newLogger(name)`
D) `logging.Logger(name)`

**CN**: `logging` 模块中，哪个方法用于创建命名日志记录器？

✅ **正确答案 / Answer: B**
> `logging.getLogger(name)` 获取或创建指定名称的日志记录器。推荐使用 `__name__` 作为参数。

---

### S2Q125
**EN**: What is the output?
```python
import logging
logging.basicConfig(level=logging.ERROR)
logging.getLogger().setLevel(logging.DEBUG)
logging.warning("Warning message")
logging.error("Error message")
```
A) Both messages are printed
B) Only "Warning message" is printed
C) Only "Error message" is printed
D) Neither message is printed

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: C**
> `basicConfig(level=logging.ERROR)` 设置根日志记录器级别为 ERROR。`logging.warning()` 级别 WARNING < ERROR，被过滤。`logging.error()` 级别等于 ERROR，被输出。

---

### S2Q126
**EN**: Which `pdb` command is used to continue execution until the next breakpoint?
A) `next`
B) `step`
C) `continue`
D) `run`

**CN**: 哪个 `pdb` 命令用于继续执行直到下一个断点？

✅ **正确答案 / Answer: C**
> `continue`（或 `c`）继续执行直到遇到下一个断点或程序结束。`next`（或 `n`）执行下一行（不会进入函数），`step`（或 `s`）进入函数内部。

---

### S2Q127
**EN**: What is the output?
```python
import traceback
try:
    raise ValueError("Error details")
except:
    tb = traceback.format_exc()
    print(type(tb).__name__)
```
A) ValueError
B) str
C) tuple
D) list

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `traceback.format_exc()` 返回异常追踪信息的字符串格式（不是直接输出）。`type(tb)` 是 `str`（字符串）。

---

### S2Q128
**EN**: Which Python module provides a simple timing/decorator for measuring execution time?
A) `timeit`
B) `profiler`
C) `timer`
D) `performance`

**CN**: 哪个 Python 模块提供简单的计时代码执行时间功能？

✅ **正确答案 / Answer: A**
> `timeit` 模块可用于测量小段代码的执行时间。`timeit.timeit(stmt, number=1000)` 执行语句指定次数并返回总时间。

---

## S2-15: 数据库 / Databases

---

### S2Q129
**EN**: What is the output?
```python
import sqlite3
conn = sqlite3.connect(':memory:')
cur = conn.cursor()
cur.execute("CREATE TABLE t (x INTEGER)")
cur.execute("INSERT INTO t VALUES (1)")
cur.execute("INSERT INTO t VALUES (2)")
conn.commit()
cur.execute("SELECT COUNT(*) FROM t")
result = cur.fetchone()
print(result[0])
```
A) 1
B) 2
C) 0
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 创建内存数据库，建表并插入两行数据后 `commit()`。`COUNT(*)` 统计行数，返回 2。

---

### S2Q130
**EN**: What is the `:memory:` parameter used for in `sqlite3.connect()`?
A) Caching query results in memory
B) Creating an in-memory database (no file on disk)
C) Storing the database in RAM for faster access
D) Creating a temporary table

**CN**: `sqlite3.connect(':memory:')` 中的 `:memory:` 参数用于什么？

✅ **正确答案 / Answer: B**
> `:memory:` 创建完全在内存中的 SQLite 数据库，不会在磁盘上创建文件。数据库在连接关闭后销毁，适用于测试和临时数据。

---

### S2Q131
**EN**: What does `cur.execute("SELECT * FROM t WHERE x > ?", (5,))` do?
A) Executes the query safely with parameter substitution
B) Concatenates the SQL string with the value 5
C) Checks if the database is valid
D) Creates a new table

**CN**: `cur.execute("SELECT * FROM t WHERE x > ?", (5,))` 的作用是什么？

✅ **正确答案 / Answer: A**
> `?` 是参数化查询占位符，值通过元组 `(5,)` 传入。这是安全做法，防止 SQL 注入攻击。注意单元素元组需要逗号 `(5,)`。

---

### S2Q132
**EN**: What is the output?
```python
import sqlite3
conn = sqlite3.connect(':memory:')
conn.execute("CREATE TABLE IF NOT EXISTS test (id INTEGER PRIMARY KEY, val TEXT)")
conn.execute("INSERT OR IGNORE INTO test VALUES (1, 'hello')")
conn.execute("INSERT OR IGNORE INTO test VALUES (1, 'world')")
print(conn.execute("SELECT val FROM test WHERE id = 1").fetchone()[0])
```
A) "hello"
B) "world"
C) "helloworld"
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: A**
> `INSERT OR IGNORE` 在冲突时忽略。两次插入 id=1，第二次因主键冲突被忽略。所以 val 为 "hello"。`fetchone()` 返回 `('hello',)`，`[0]` = "hello"。

---

### S2Q133
**EN**: What is the output?
```python
import sqlite3
with sqlite3.connect(':memory:') as conn:
    conn.execute("CREATE TABLE t (x)")
    conn.execute("INSERT INTO t VALUES (10)")
    conn.execute("INSERT INTO t VALUES (20)")
    cur = conn.execute("SELECT x FROM t ORDER BY x DESC")
    rows = cur.fetchall()
    print(rows[0][0])
```
A) 10
B) 20
C) [10, 20]
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> 使用 `with` 语句管理连接。`ORDER BY x DESC` 按 x 降序排列。结果为 `(20,), (10,)`。`rows[0][0]` = 20。

---

### S2Q134
**EN**: What does `cursor.fetchmany(3)` return if there are only 5 rows in total?
A) Exactly 3 rows
B) All 5 rows
C) A list of up to 3 rows
D) An error

**CN**: 如果总共只有 5 行数据，`cursor.fetchmany(3)` 返回什么？

✅ **正确答案 / Answer: C**
> `fetchmany(size)` 返回最多 `size` 行的列表。如果有 5 行，调用 `fetchmany(3)` 返回 3 行。如果不足 3 行，返回剩余行数（不报错）。

---

### S2Q135
**EN**: What is the output?
```python
import sqlite3
conn = sqlite3.connect(':memory:')
conn.execute("CREATE TABLE t (a, b)")
conn.execute("INSERT INTO t VALUES (1, 'x')")
cur = conn.execute("SELECT * FROM t")
row = cur.fetchone()
print(len(row))
```
A) 1
B) 2
C) 0
D) Error

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `SELECT * FROM t` 选择表 t 的所有列（a 和 b）。`fetchone()` 返回一个元组 `(1, 'x')`，长度为 2（两列）。

---

### S2Q136
**EN**: After calling `connection.close()`, which statement is TRUE?
A) The connection can still execute queries
B) Any uncommitted changes are lost
C) The database file is deleted
D) A new connection can be opened from the same cursor

**CN**: 调用 `connection.close()` 后，哪个说法是正确的？

✅ **正确答案 / Answer: B**
> 关闭连接后未提交（uncommitted）的更改将丢失。连接关闭后不能再执行查询（A 错）。游标在连接关闭后也失效（D 错）。

---

## S2-16: 网络与项目 / Networking & Project

---

### S2Q137
**EN**: What is the output?
```python
import socket
print(type(socket.gethostbyname('localhost')))
```
A) `<class 'int'>`
B) `<class 'str'>`
C) `<class 'tuple'>`
D) `<class 'list'>`

**CN**: 以下代码的输出是什么？

✅ **正确答案 / Answer: B**
> `socket.gethostbyname('localhost')` 返回 IP 地址字符串 `"127.0.0.1"`，类型为 `str`。

---

### S2Q138
**EN**: Which of the following is a well-known port for HTTPS?
A) 80
B) 443
C) 8080
D) 22

**CN**: 以下哪个是 HTTPS 的知名端口？

✅ **正确答案 / Answer: B**
> HTTPS 使用端口 443。HTTP 使用 80，SSH 使用 22，8080 常用于 HTTP 测试/代理。

---

### S2Q139
**EN**: In a TCP server, what is the correct order of socket operations?
A) socket → bind → listen → accept
B) socket → listen → bind → accept
C) socket → connect → bind → listen
D) socket → accept → bind → listen

**CN**: TCP 服务器中 socket 操作的正确顺序是什么？

✅ **正确答案 / Answer: A**
> TCP 服务器标准步骤：1) `socket()` 创建 socket，2) `bind()` 绑定地址和端口，3) `listen()` 开始监听，4) `accept()` 接受客户端连接。

---

### S2Q140
**EN**: What is the purpose of `socket.bind()`?
A) To connect to a remote server
B) To assign an IP address and port number to a socket
C) To start listening for connections
D) To close a socket

**CN**: `socket.bind()` 的作用是什么？

✅ **正确答案 / Answer: B**
> `bind((host, port))` 将 socket 绑定到指定 IP 地址和端口。服务端需要先 bind 再 listen。

---

### S2Q141
**EN**: What is a "project skeleton" in Python development?
A) The minimum viable code required for a Git repository
B) A template or directory structure for starting a new Python project
C) A tool for removing unused code
D) A Python code obfuscator

**CN**: Python 开发中的"项目骨架(project skeleton)"是什么？

✅ **正确答案 / Answer: B**
> 项目骨架是 Python 项目的标准目录结构和配置模板，通常包括 `setup.py`、`README.md`、`tests/`、`src/` 等。可以使用 `cookiecutter` 等工具自动生成。

---

### S2Q142
**EN**: What port number range requires superuser/root privileges to bind to on Unix systems?
A) 0-1023
B) 1024-49151
C) 49152-65535
D) All ports

**CN**: Unix 系统上绑定哪些端口范围需要超级用户/root 权限？

✅ **正确答案 / Answer: A**
> 端口 0-1023 是"知名端口"(well-known ports)，绑定这些端口需要 root 权限。1024-49151 是注册端口，49152-65535 是动态/私有端口。

---

> **第二套共 142 道全新题目**（S2Q1-S2Q142），与第一套 195 道题无重复。完整覆盖 SHL Python 3.7 考试全部考点。
>
> **复习建议**: 两套题库共 337 题，建议先做完第一套再练习第二套，确保每种题型都充分练习。
>
> **祝考试顺利！Good luck with your exam! 🎓**
