## Time complexity

#### 1. 衡量程序算法执行时间的2种方法

1) 事后统计

但是这种方法存在缺陷：

a) 需要实际运行程序

b) 所得时间和计算机的硬件、软件及环境因素有关，为了保证衡量的科学性，很难保证计算机处于相同的状态



2) 根据**时间复杂度**来判断

算法的执行时间和算法中语句的执行次数成正比例

- 忽略常数项
- 忽略低次项
- 忽略系数（但是这个取决于最高此项是几次方）

算法基本执行语句的重复次数是问题规模n的函数 T(n)，我们借助辅助函数f(n)，当n趋近于无穷大时，T(n)/f(n)的极限值等于一个不等于0的常数，记作 T(n) = O(f(n))，称为**算法的渐进时间复杂度**，简称为“时间复杂度”。



#### 2. 常见时间复杂度

1) 常数阶 $O\left( 1 \right)$

```java
int i = 1;
int j = 2;
++i;
++j;
int m = i + j;
```

只要没有循环等复杂结构，代码再长也是O(1)的时间复杂度



2) 对数阶 $O\left( \log _2n \right)$

```java
int i = 1;
while(i<n)
{
	i = i * 2;
}
```

底数取决于循环体中的具体数字，比如如果while循环体中是 i=i*3; 那么时间复杂度就是 $O\left( \log _3n \right)$



3) 线性阶 $O\left( n \right)$

```java
for (int i=0;i<n;i++)
{
    j = i;
    j++;
}
```



4) 线性对数阶 $O\left( n\log n \right)$

```java
for (int m=0;m<n;m++)
{
    int i = 1;
    while(i<n)
    {
        i = i * 2;
    }
}
```

这种也很好了解，就是对数阶外层有另外一层n循环



5) 平方阶 $O\left( n^2 \right)$

```java
for (int x=0;x<n;x++)
{
    for (int i=0;i<n;i++)
    {
        j = i;
        j++;
    }
}
```

最常见的双层循环



其他常见的时间复杂度和上面的类似。

6) 立方阶 $O\left( n^3 \right)$

7) k次方阶 $O\left( n^k \right)$

8) 指数阶 $O\left( 2^n \right)$



常见的时间复杂度从小到大排列依次为：$O\left( 1 \right)$ < $O\left( \log _2n \right)$ < $O\left( n \right)$ <  $O\left( n^2 \right)$ < $O\left( n^3 \right)$ < $O\left( n^k \right)$ < $O\left( 2^n \right)$

因此我们要避免使用指数阶的时间复杂度



#### 平均时间复杂度 & 最坏时间复杂度



## Space complexity

空间复杂度指的是一个算法在运行过程中临时占用的存储空间的大小





