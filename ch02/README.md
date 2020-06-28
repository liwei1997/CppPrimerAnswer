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
>**(a)** `'a', L'a', "a", L"a"`  
>**(b)** `10, 10u, 10uL, 012, 0xC`  
>**\(c\)** `3.14, 3.14f, 3.14L,`  
>**(d)** `10, 10u, 10., 10e-2`

#### 练习 2.6
>下面两组定义是否有区别，如果有，请叙述之：
>
>```c++
>int month = 9, day = 7;
>int month = 09, day = 07;
>```

#### 练习 2.7
>下述字面值表示何种含义？它们各自的数据类型是什么？  
>**(a)** `"Who goes with F\145rgus?\012"`  
**(b)** `3.14e1L`  
>**\(c\)** `1024f`  
>**(d)** `3.14L`

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
>**(a)** `std::cin >> int input_value;`  
>**(b)** `int i = { 3.14 };`  
>**\(c\)** `double salary = wage = 9999.99;`  
>**(d)** `int i = 3.14;`

#### 练习 2.10
>下列变量的初始值分别是什么？
>
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
>**(a)** `extern int ix = 1024;`  
>**(b)** `int iy;`  
>**\(c\)** `extern int iz;`

### 2.2.3 标识符
#### 练习 2.12
>请指出下列的名字中哪些是非法的？  
>**(a)** `int double = 3.14;`  
>**(b)** `int _;`  
>**\(c\)** `int catch-22;`  
>**(d)** `int 1_or_2 = 1;`  
>**(e)** `double Double = 3.14;`  

### 2.2.4 名字的作用域
#### 练习 2.13
>下面程序中`j`的值是多少？
>
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
>
>```c++
>int i = 100; sum = 0;
>for (int i = 0; i != 10; ++i)
>    sum += i;
>std::cout << i << " " << sum << std::endl;
>```

## 2.3 复合类型
### 2.3.1 引用
#### 练习 2.15
>下面的哪个定义是不合法的？为什么？  
>**(a)** `int ival = 1.01;`  
>**(b)** `int &rval1 = 1.01;`  
>**\(c\)** `int &rval2 = ival;`  
>**(d)** `int &rvall3;`

#### 练习 2.16
>考查下面的所有赋值然后回答：哪些赋值是不合法的？为什么？哪些赋值是合法的？它们执行了什么样的操作？  
>
>```c++
>int i = 0, &r1 = i;
>double d = 0, &r2 = d;
>```
>**(a)** `r2 = 3.14159;`  
>**(b)** `r2 = r1;`  
>**\(c\)** `i = r2;`  
>**(d)** `r1 = d;`  

#### 练习 2.17
>执行下面的代码段将输出什么结果？
>
>```c++
>int i, &ri = i;
>i = 5;
>ri = 10;
>std::cout << i << " " << ri << std::endl;
>```

### 2.3.2 指针
#### 练习 2.18
>编写代码分别更改指针的值以及指针所指对象的值。
>
>```c++
>#include <iostream>
>
>int main()
>{
>    int i = 24;
>    int *pi = &i;
>    std::cout << pi << " " << *pi << std::endl;
>    *pi = 10;
>    std::cout << pi << " " << *pi << std::endl;
>    pi = 0;
>    std::cout << pi << std::endl;
>    return 0;
>}
>```

#### 练习 2.19
>说明指针和引用的主要区别。

#### 练习 2.20
>请叙述下面这段代码的作用。
>
>```c++
>int i = 42;
>int *p1 = &i;
>*p1 = *p1 * *p1;
>```

#### 练习 2.21
>
>```c++
>int i = 0;
>```
>**(a)** `double *dp = &i;`  
>**(b)** `int *ip = i;`  
>**\(c\)** `int *p = &i;`

#### 练习 2.22
>假设p是一个int型指针，请说明下述代码的含义。
>
>```c++
>if (p) // ...
>if (*p) // ...
>```

#### 练习 2.23
>给定指针p，你能知道它是否指向了一个合法的对象吗？如果能，叙述判断的思路；如果不能，也请说明原因。

#### 练习 2.24
>在下面这段代码中为什么p合法而lp非法？
>
>```c++
>int i = 42;
>void *p = &i;
>long *lp = &i;
>```

### 2.3.3 理解复合类型的声明
#### 练习 2.25
>说明下列变量的类型和值。  
>**(a)** `int *ip, i, &r = i;`  
>**(b)** `int i, *ip = 0;`  
>**\(c\)** `int * ip, ip2;`

## 2.4 const 限定符
#### 练习 2.26
>下面哪些句子是合法的？如果有不合法的句子，请说明为什么？  
>**(a)** `const int buf;`  
>**(b)** `int cnt = 0;`  
>**\(c\)** `const int sz = cnt;`  
>**(d)** `++cont; ++sz;`

### 2.4.1 const 的引用
### 2.4.2 指针和 const
#### 练习 2.27
> 下面的哪些初始化是合法的？请说明原因。  
>**(a)** `int i = -1, &r = 0;`  
>**(b)** `int const p2 = &i2;`  
>**\(c\)** `const int i = -1, &r = 0;`  
>**(d)** `const int *const p3 = &i2;`  
>**(e)** `const int *p1 = &i2;`  
>**(f)** `const int &const r2;`  
>**(g)** `const int i2 = i, &r = i;`

#### 练习 2.28
>说明下面的这些定义是什么意思，挑出其中不合法的。  
>**(a)** `int i, *const cp;`  
>**(b)** `int *p1, *const p2;`  
>**\(c\)** `const int ic, &r = ic;`  
>**(d)** `const int *const p3;`  
>**(e)** `const int *p;`

#### 练习 2.29
>假设已有上一个练习中定义的哪些变量，则下面的哪些语句是合法的？请说明原因。  
>**(a)** `i = ic;`  
>**(b)** `p1 = p3;`  
>**\(c\)** `p1 = &ic;`  
>**(d)** `p3 = &ic;`  
>**(e)** `p2 = p1;`  
>**(f)** `ic = *p3;`

### 2.4.3 顶层 const
#### 练习 2.30
>对于下面的这些语句，请说明对象被声明成了顶层const还是底层const？
>
>```c++
>const int v2 = 0;
>int v1 = v2;
>int *p1 = &v1, &r1 = v1;
>const int *p = &v2, *const p3 = &i, &r2 = v2;
>```

#### 练习 2.31
>假设已有上一个练习中所做的哪些声明，则下面的哪些语句是合法的？请说明顶层 const 和底层 const 在每个例子中有何体现。
>
>```c++
>r1 = v2;
>p1 = p2; p2 = p1;
>p1 = p3; p2 = p3;
>```

### 2.4.4 constexpr 和常量表达式
#### 练习 2.32
>下面的代码是否合法？如果合法，请设法将其修改正确。
>
```c++
int null = 0, *p = null;
```

## 2.5 处理类型
### 2.5.1 类型别名
### 2.5.2 auto 类型说明符
#### 练习 2.33
>利用本节定义的变量，判断下列语句的运行结果。
>
>```c++
>a = 42;
>b = 42;
>c = 42;
>d = 42;
>e = 42;
>g = 42;
>```

#### 练习 2.34
>基于上一个练习中的变量和语句编写一段程序，输出赋值前后变量的内容，你刚才的推断正确吗？如果不正确，请反复研读本节的示例直到你明白错在何处为止。

```c++
#include <iostream>

int main()
{
    int i = 0, &r = i;
    const int ci = i, &cr = ci;
    auto a = r;  // a: int
    auto b = ci;  // b: int
    auto c = cr;  // c: int
    auto d = &i;  // d: int *
    auto e = &ci;  // e: const int *
    auto &g = ci;  // g: int &;
    std::cout
        << a << "\n" 
        << b << "\n"
        << c << "\n"
        << d << "\n"
        << e << "\n"
        << g << "\n" 
        << std::endl;
    a = 42;
    b = 42; 
    c = 42;
    //d = 42; e = 42; g = 42;
    std::cout
        << a << "\n" 
        << b << "\n"
        << c << "\n"
        << d << "\n"
        << e << "\n"
        << g << "\n" 
        << std::endl;
    return 0;
}
```

#### 练习 2.35
>请判断下列定义推断出的类型是什么，然后编写程序进行验证。
>
>```c++
>const int i = 42;
>auto j = i;
>const auto &k = i;
>auto *p = &i;
>const auto j2 = i, &k2 = i;
>```

```c++
#include <iostream>
int main()
{
    const int i = 42;
    auto j = i;  // j: int
    const auto &k = i;  // k: const int &
    auto *p = &i;  // p: const int *
    const auto j2 = i, &k2 = i;  // j2: const int, k2: const int &
    j = 24;  // true
    // k = 42;  // false
    const int j1 = 42;
    p = &j1;  // true
    // int &r = j2;  // false
    // k2 = 25;  // false
    return 0;
}
```
### 2.5.3 decltype 类型指示符
#### 练习 2.36
>关于下面的代码，请指出每一个变量的类型以及程序结束时它们各自的值。
>
```c++
int a = 3, b = 4;
decltype(a) c = a;
decltype ((b)) = a;
++c;
++d;
```
#### 练习 2.37
>赋值是会产生引用的一类典型表达式，引用的类型就是左值的类型。也就是说，如果i是int，则表达式i=x的类型是int&。根据这一特点，请指出下面的代码中每一个变量的类型和值。

```c++
int a = 3, b = 4;
decltype(a) c = a;
decltype(a = b) d = a;
```
#### 练习 2.38
>说明由decltype指定类型和由auto指定类型有何区别。请举出一个例子，decltype指定的类型与auto指定的类型一样；再举一个例子，decltype指定的类型与auto指定的类型不一样。

```c++
#include <iostream>
int main()
{
    int i = 10, &j = i;
    // same
    auto a = i;
    decltype(i) a1;
    // different 
    auto b = j;  //b: int
    decltype(j) b1 = i;  //b1: int &
    return 0;
}
```
## 2.6 自定义数据结构
### 2.6.1 定义Sales_data类型
#### 练习 2.39
>编译下面的程序观察其运行结果，注意，如果忘记写类定义体后边的分号会发生什么情况？记录下相关信息，以后可能会有用。
>
>```c++
>struct Foo { /* 此处为空 */ } // 注意：没有分号
>int main()
>{
>    return 0;
>}
>```

#### 练习 2.40
>根据自己的理解写出Sales_data类，最好与书中的例子有所区别。

```c++
struct Sales_data {
    std::string ISBN;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};
```
#### 练习 2.41
>使用你自己的Sales_data类重写1.51节、1.52节、1.6节的练习。眼下先把Sales_data类的定义和`main`函数放在同一个文件里。

```c++
/* 练习1.20*/
#include <iostream>
#include <string>

struct Sales_data {
    std::string isbn;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};

int main()
{
    Sales_data book;
    while (std::cin >> book.ISBN >> book.numbers >> book.price) {
        book.total = book.numbers * book.price;
        std::cout << book.ISBN << " " << book.numbers << " " << book.price << " " << book.total << std::endl;
    }
    return 0;
}
```
```c++

/* 练习1.21*/
#include <iostream>
#include <string>

struct Sales_data {
    std::string ISBN;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};

int main()
{
    Sales_data book, book2;
    std::cin >> book.ISBN >> book.numbers >> book.price;
    book.total = book.numbers * book.price;
    std::cin >> book2.ISBN >> book2.numbers >> book2.price;
    book2.total = book2.numbers * book2.price;
    if (book.ISBN == book2.ISBN) {
        book.numbers += book2.numbers;
        book.total += book2.total;
        std::cout << book.ISBN << " " << book.numbers << " " << book.total << std::endl;
        return 0;
    } else {
        std::cerr << "Data must refer to the same ISBN." << std::endl;
        return -1;
    }
}
```
```c++

/* 练习1.22*/
#include <iostream>
#include <string>

struct Sales_data {
    std::string ISBN;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};

int main()
{
    Sales_data books;
    if (std::cin >> books.ISBN >> books.numbers >> books.price) {
        books.total = books.numbers * books.price;
        Sales_data books2;
        while (std::cin >> books2.ISBN >> books2.numbers >> books2.price) {
            books2.total = books2.numbers * books2.price;
            if (books.ISBN == books2.ISBN) {
                books.numbers += books2.numbers;
                books.total += books2.total;
            }
        }
        std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1;
    }
    return 0;
}
```
```c++
/* 练习1.23*/
#include <iostream>
#include <string>

struct Sales_data {
    std::string ISBN;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};

int main()
{
    Sales_data books;
    if (std::cin >> books.ISBN >> books.numbers >> books.price) {
        books.total = books.numbers * books.price;
        int count = 1;
        Sales_data books2;
        while (std::cin >> books2.ISBN >> books2.numbers >> books2.price) {
            books2.total = books2.numbers * books2.price;
            if (books.ISBN == books2.ISBN) {
                books.numbers += books2.numbers;
                books.total += books2.total;
                ++count;
            } else {
                std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
                std::cout << count << std::endl;
                count = 1;
                books = books2;
            }
        }
        std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
        std::cout << count << std::endl;
        return 0;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1;
    }
}
```
```c++

/* 练习1.25*/
#include <iostream>
#include <string>

struct Sales_data {
    std::string ISBN;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};

int main()
{
    Sales_data books;
    if (std::cin >> books.ISBN >> books.numbers >> books.price) {
        books.total = books.numbers * books.price;
        Sales_data books2;
        while (std::cin >> books2.ISBN >> books2.numbers >> books2.price) {
            books2.total = books2.numbers * books2.price;
            if (books.ISBN == books2.ISBN) {
                books.numbers += books2.numbers;
                books.total += books2.total;
            } else {
                std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
                books = books2;
            }
        }
        std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
        return 0;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1;
    }
}
```
### 2.6.3 编写自己的头文件
### 练习 2.42
>根据你自己的理解重写一个Sales_data.h头文件，并以此为基础重做2.6.2节的练习。

```c++
/* Sales_data.h */
#ifndef SALES_DATA_H
#define SALES_DATA_H
#include <string>

struct Sales_data {
    std::string ISBN;
    unsigned numbers = 0;
    double price = 0.0;
    double total = 0.0;
};

#endif
```
```c++
#include <iostream>
#include "Sales_data.h"

int main()
{
    Sales_data book;
    while (std::cin >> book.ISBN >> book.numbers >> book.price) {
        book.total = book.numbers * book.price;
        std::cout << book.ISBN << " " << book.numbers << " " << book.price << " " << book.total << std::endl;
    }
    return 0;
}

```
```c++
#include <iostream>
#include "Sales_data.h"

int main()
{
    Sales_data book, book2;
    std::cin >> book.ISBN >> book.numbers >> book.price;
    book.total = book.numbers * book.price;
    std::cin >> book2.ISBN >> book2.numbers >> book2.price;
    book2.total = book2.numbers * book2.price;
    if (book.ISBN == book2.ISBN) {
        book.numbers += book2.numbers;
        book.total += book2.total;
        std::cout << book.ISBN << " " << book.numbers << " " << book.total << std::endl;
        return 0;
    } else {
        std::cerr << "Data must refer to the same ISBN." << std::endl;
        return -1;
    }
}

```
```c++
#include <iostream>
#include "Sales_data.h"

int main()
{
    Sales_data books;
    if (std::cin >> books.ISBN >> books.numbers >> books.price) {
        books.total = books.numbers * books.price;
        Sales_data books2;
        while (std::cin >> books2.ISBN >> books2.numbers >> books2.price) {
            books2.total = books2.numbers * books2.price;
            if (books.ISBN == books2.ISBN) {
                books.numbers += books2.numbers;
                books.total += books2.total;
            }
        }
        std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1;
    }
    return 0;
}

```
```c++
#include <iostream>
#include "Sales_data.h"

int main()
{
    Sales_data books;
    if (std::cin >> books.ISBN >> books.numbers >> books.price) {
        books.total = books.numbers * books.price;
        int count = 1;
        Sales_data books2;
        while (std::cin >> books2.ISBN >> books2.numbers >> books2.price) {
            books2.total = books2.numbers * books2.price;
            if (books.ISBN == books2.ISBN) {
                books.numbers += books2.numbers;
                books.total += books2.total;
                ++count;
            } else {
                std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
                std::cout << count << std::endl;
                count = 1;
                books = books2;
            }
        }
        std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
        std::cout << count << std::endl;
        return 0;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1;
    }
}

```
```c++
#include <iostream>
#include "Sales_data.h"

int main()
{
    Sales_data books;
    if (std::cin >> books.ISBN >> books.numbers >> books.price) {
        books.total = books.numbers * books.price;
        Sales_data books2;
        while (std::cin >> books2.ISBN >> books2.numbers >> books2.price) {
            books2.total = books2.numbers * books2.price;
            if (books.ISBN == books2.ISBN) {
                books.numbers += books2.numbers;
                books.total += books2.total;
            } else {
                std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
                books = books2;
            }
        }
        std::cout << books.ISBN << " " << books.numbers << " " << books.total << std::endl;
        return 0;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1;
    }
}
```
