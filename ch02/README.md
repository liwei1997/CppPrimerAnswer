# 第二章 变量和基本类型
## 2.1 基本内置类型
### 2.1.1 算术类型
#### 练习 2.1
>类型int、long、longlong和short的区别是什么？无符号类型和带符号类型的区别是什么？float和double的区别是什么？

#### 练习 2.2
>计算按揭贷款时，对于利率、本金和付款分别应选择何种数据类型？说明你的理由。

### 2.1.2 类型转换
#### 练习 2.3
>读程序写结果。
>
>```
>unsigned u = 10, u2 = 42;`  
>std::cout << u2 - u << std::endl;
>std::cout << u - u2 << std::endl;
>
>int i = 10, i2 = 42;`  
>std::cout << i2 - i << std::endl;
>std::cout << i - i2 << std::endl;
>std::cout << i - u << std::endl;
>std::cout << u - i << std::endl;
>```

#### 练习 2.4
>编写程序检查你的估计是否正确，如果不正确，请仔细研读本节知道弄明白问题所在。

### 2.1.3 字面值常量
#### 练习 2.5
>指出下述字面值的数据类型并说明每一组内几种字面值的区别：  
>**(a)** 'a', L'a', "a", L"a"  
>**(b)** 10, 10u, 10uL, 012, 0xC  
>**\(c\)** 3.14, 3.14f, 3.14L,  
>**(d)** 10, 10u, 10., 10e-2

#### 练习 2.6
>下面两组定义是否有区别，如果有，请叙述之：
>
>```c++
>int month = 9, day = 7;
>int month = 09, day = 07;
>```

#### 练习 2.7
>下述字面值表示何种含义？它们各自的数据类型是什么？  
>**(a)** "Who goes with F\145rgus?\012"  
**(b)** 3.14e1L  
>**\(c\)** 1024f  
>**(d)** 3.14L

#### 练习 2.8
>请利用转义序列编写一段程序，要求先输出2M，然后转到新一行。修改程序使其先输出2，然后输出制表符，再输出M，最后转到新一行。
```c++
#include <iostream>

int main()
{
    std::cout << "2M\n" << std::endl;
    return 0;
}
```
```c++
#include <iostream>

int main()
{
    std::cout << "2\tM\n" << std::endl;
    return 0;
}
```
## 2.2 变量
### 2.2.1 变量定义
#### 练习 2.9
>解释下列定义的含义。对于非法的定义，请说明错在何处并将其改正。
>**(a)** std::cin >> int input_value;  
>**(b)** int i = { 3.14 };  
>**\(c\)** double salary = wage = 9999.99;  
>**(d)** int i = 3.14;

#### 练习 2.10
>下列变量的初始值分别是什么？
>```c++
>std::string global_str;
>int global_int;
>int main()
>{
>    int local_int;
>    std::string local_str;
>}
>```

### 2.2.2 变量声明和定义的关系
#### 练习 2.11
>**(a)** extern int ix = 1024;  
>**(b)** int iy;  
>**\(c\)** extern int iz;

### 2.2.3 标识符
#### 练习 2.12
>请指出下列的名字中哪些是非法的？  
>**(a)** int double = 3.14;  
>**(b)** int _;  
>**\(c\)** int catch-22;  
>**(d)** int 1_or_2 = 1;  
>**(e)** double Double = 3.14;  

### 2.2.4 名字的作用域
#### 练习 2.13
>下面程序中`j`的值是多少？
>```c++
>int i = 42;
>int main()
>{
>    int i = 100;
>    int j = i;
>}
>```

#### 练习 2.14
>下面的程序合法吗？如果合法，它将输出什么？
>```c++
>int i = 100; sum = 0;
>for (int i = 0; i != 10; ++i)
>    sum += i;
>std::cout << i << " " << sum << std::endl;
>```

## 2.3 复合类型
### 2.3.1 引用
<++>
