# list、tuple、dict、set

* list []
* tuple ()
* dict {}
* set ([])

# 定义函数

def fun(x):

​	x

​	return x

- 如果没有`return`语句，函数执行完毕后也会返回结果，只是结果为`None`。`return None`可以简写为`return`

- 在定义空函数或者if中不放操作的时候防止报错可以使用pass

## 参数提示设置

```python
isinstance(x, (int, float))：#如果x属于int、float则返回ture
```

```python
#python中单行注释

'''
多行注释1
'''

"""
多行注释2
"""
```

Python的函数返回多值其实就是返回一个tuple

## 可变参数

在参数前+`*`则在函数中接收到的是一个`tuple`

而且在可变参数的函数中传入已有tuple时，在已有的tuple或者list前面+一个`*`即可

## Iterable、Iterator

凡是可作用于`for`循环的对象都是`Iterable`类型；

凡是可作用于`next()`函数的对象都是`Iterator`类型，它们表示一个惰性计算的序列；

集合数据类型如`list`、`dict`、`str`等是`Iterable`但不是`Iterator`，不过可以通过`iter()`函数获得一个`Iterator`对象。

# 模块

## 作用域

`_xxx`和`__xxx`这样的函数或变量就是非公开的（private）

`__xxx__`这样的变量是特殊变量，可以被直接引用，但是有特殊用途

正常的函数和变量名是公开的（public），可以被直接引用