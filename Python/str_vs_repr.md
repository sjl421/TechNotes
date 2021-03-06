# str vs repr

`str()`与`repr()`都是Python的内建函数,通过它们可以方便地以字符串的方式获取对象的内容、类型、数值属性等信息。大多数情况下他们的效果相同，但是既然是不同的函数肯定有不同的地方，概括起来可以这样说<font color='red'>`str()`会将对象转化为可读性较好的字符串，而`repr()`会将对象转化为供解释器读取形式的字符串</font>。一个对象没有适于人阅读的解释形式的话，`str()`会返回与`repr()`相同的值。
其中，数值或list、tuple、字典等这样的结构，针对各种函数都有着统一的解读方式。而字符串不同函数可能有着不同的解读方式。


```
>>> str(123)
'123'
>>> repr(123)
'123'
>>> str((1, 2, 3, 4, 5))
'(1, 2, 3, 4, 5)'
>>> repr((1, 2, 3, 4, 5))
'(1, 2, 3, 4, 5)'
>>> str([1, 2, 3, 4, 5])
'[1, 2, 3, 4, 5]'
>>> repr([1, 2, 3, 4, 5])
'[1, 2, 3, 4, 5]'
>>> str({1: 2, 3: 4})
'{1: 2, 3: 4}'
>>> repr({1: 2, 3: 4})
'{1: 2, 3: 4}'
>>> str(4.53-2j)
'(4.53-2j)'
>>> repr(4.53-2j)
'(4.53-2j)'
>>> str(2e10)
'20000000000.0'
>>> repr(2e10)
'20000000000.0'
```

```
>>> hi = 'hello world\n Python'
>>> hi
'hello world\n Python'
>>> str(hi)
'hello world\n Python'
>>> repr(hi)
"'hello world\\n Python'"

>>> print(str(hi))
hello world
 Python
>>> print(repr(hi))
'hello world\n Python'

```




