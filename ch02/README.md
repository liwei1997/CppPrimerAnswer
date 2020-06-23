# 第二章 变量和基本类型
## 2.1.1 节练习
### 练习 2.1
>类型int、long、longlong和short的区别是什么？无符号类型和带符号类型的区别是什么？float和double的区别是什么？

### 练习 2.2
>计算按揭贷款时，对于利率、本金和付款分别应选择何种数据类型？说明你的理由。

## 2.1.2 节练习
### 练习 2.3
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

### 练习 2.4
>编写程序检查你的估计是否正确，如果不正确，请仔细研读本节知道弄明白问题所在。

## 2.1.3 节练习
### 练习 2.5
>指出下述字面值的数据类型并说明每一组内几种字面值的区别：  
>**(a)** 'a', L'a', "a", L"a"  
>**(b)** 10, 10u, 10uL, 012, 0xC  
>**\(c\)** 3.14, 3.14f, 3.14L,  
>**(d)** 10, 10u, 10., 10e-2

### 练习 2.6
>下面两组定义是否有区别，如果有，请叙述之：
>
>```c++
>int month = 9, day = 7;
>int month = 09, day = 07;
>```

### 练习 2.7
>下述字面值表示何种含义？它们各自的数据类型是什么？  
>**(a)** "Who goes with F\145rgus?\012"  
**(b)** 3.14e1L  
>**\(c\)** 1024f  
>**(d)** 3.14L

### 练习 2.8
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

