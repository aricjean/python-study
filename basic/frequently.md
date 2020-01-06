## 内置常见
```python
print("Hello, world!") # 会输出换行
print("Hello, world!", end="") # 将末尾的字符替换为空字符（也就是没有换行了）
```

```python
a = input("\n\n按下 enter 键后退出。")
```

```python
a = 111
type(a) # <class 'int'> # type()不会认为子类是一种父类类型
isinstance(a, int) # True  # isinstance()会认为子类是一种父类类型
```

```python
# 如

class A:
    pass

class B(A):
     pass

isinstance(A(), A) # True
type(A()) == A  # True
isinstance(B(), A) # True
type(B()) == A # False
```

### String
```python
a = "1 2 3 4"
a.split(" ") # ["1","2","3","4"]
```


### List
```python
append()
pop()
```

### 迭代器
```python
>>> list=[1,2,3,4]
>>> it = iter(list)    # 创建迭代器对象
>>> print (next(it))   # 输出迭代器的下一个元素
1
>>> print (next(it))
2
>>>
```
```python
#!/usr/bin/python3
 
list=[1,2,3,4]
it = iter(list)    # 创建迭代器对象
for x in it:
    print (x, end=" ")
```


### 模块
```python
#!/usr/bin/python3
# 文件名: using_sys.py
import sys
print('命令行参数如下:')
for i in sys.argv:
   print(i)

print('\n\nPython 路径为：', sys.path, '\n')
```
```python
python using_sys.py 参数1 参数2
```
输出：
using_sys.py
参数1
参数2

Python 路径为： ['/root', '/usr/lib/python3.4', '/usr/lib/python3.4/plat-x86_64-linux-gnu', '/usr/lib/python3.4/lib-dynload', '/usr/local/lib/python3.4/dist-packages', '/usr/lib/python3/dist-packages'] 

1. import sys 引入 python 标准库中的 sys.py 模块；这是引入某一模块的方法。
2. sys.argv 是一个包含命令行参数的列表。
3. sys.path 包含了一个 Python 解释器自动查找所需模块的路径的列表。

#### __name__属性
一个模块被另一个程序第一次引入时，其主程序将运行。如果我们想在模块被引入时，模块中的某一程序块不执行，我们可以用__name__属性来使该程序块仅在该模块自身运行时执行。

```python
#!/usr/bin/python3
# Filename: using_name.py

if __name__ == '__main__':
   print('程序自身在运行')
else:
   print('我来自另一模块')

```

```bash
$ python using_name.py
程序自身在运行
$ python
>>> import using_name
我来自另一模块
>>>
```
说明： 每个模块都有一个__name__属性，当其值是'__main__'时，表明该模块自身在运行，否则是被引入。
说明：__name__ 与 __main__ 底下是双下划线， _ _ 是这样去掉中间的那个空格。

#### dir() 函数
内置的函数 dir() 可以找到模块内定义的所有名称。以一个字符串列表的形式返回:












