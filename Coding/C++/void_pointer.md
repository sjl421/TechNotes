
# void指针

## 定义

void 即『无类型』，`void *` 则为『无类型指针』，可以指向任何数据类型。
void 指针可以指向任意类型的数据，亦即可用任意数据类型的指针对 void 指针赋值。


```
void *p1;
int *p2;

p1 = p2;        //任意数据类型的指针对void指针赋值
p2 = (int *)p1; //void指针赋给其他类型指针，需要强制类型转换
```

## void指针使用

> 由于void指针可以指向任意类型的数据，因此可以用void指针来作为函数形参，这样函数就可以接受任意数据类型的指针作为参数。 