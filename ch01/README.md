## 1.1 节练习
### 练习 1.1
>查阅你使用的编译器的文档，确定它所使用的文件命名约定，编译并运行第 2 页的 main 程序。
### 练习 1.2
>改写程序，让它返回 -1 。返回值 -1 通常被当作程序错误的标识。重新编译并运行你的程序，观察你的系统如何处理 main 返回的错误标识。
## 1.2 节练习
### 练习 1.3
>编写程序，在标准输出上打印 Hello, World.
```c++
#include <iostream>

int main()
{
    std::cout << "Hello, World." << std::endl
    return 0;
}
```
### 练习 1.4
>我们的程序使用加法运算符`+`来将两个数相加。编写程序使用乘法运算符`*`,来打印两个数的积。
```c++
#include <iostream>

int main()
{
    std::cout << "Enter two numbers:" << std::endl;
    int v1 = 0, v2 = 0;
    std::cin >> v1 >> v2;
    std::cout << "The product of " v1 << " and " << v2 << " is " << v1*v2 << std::endl;
    return 0;
}
```
### 练习1.5
>我们将所有输出操作放在一条很长的语句中。重写程序，将每个运算对象的打印操作放在一条独立的语句中。
```c++
#include <iostream>

int main()
{
    std::cout << "Enter two numbers:" << std::endl;
    int v1 = 0, v2 = 0;
    std::cin >> v1 >> v2;
    std::cout << "The sum of ";
    std::cout << v1;
    std::cout << " and ";
    std::cout << v2;
    std::cout << " is ";
    std::cout << v1+v2;
    std::cout << std::endl;
    return 0;
}
```
### 练习 1.6
>解释下面程序片段是否合法。
>```c++
>std::cout << "The sum of " << v1;
>          << " and " << v2;
>          << " is " << v1+v2 << std::endl;
>```
>如果程序是合法的，它输出什么？如果程序不合法，原因何在？应该如何修正？
## 1.3 节练习
### 练习 1.7
>编译一个包含不正确的嵌套注释的程序，观察编译器返回的错误信息。
### 练习 1.8
>指出下列那些输出语句是合法的：  
>`std::cout << "/*";`  
>`std::cout << "*/";`  
>`std::cout << /* "*/" */;`  
>`std::cout << /* "*/" /* "/*" */;`  
>预测编译这些语句回产生什么样的结果，实际编译这些语句来验证你的答案（编写一个小程序，每次将上述一条语句作为其主体），改正每个编译错误。
## 1.4.1 节练习
### 练习 1.9
>编写程序，使用while循环将50到100的整数相加。
```c++
include <iostream>

int main()
{
    int sum = 0,val = 50;
    while (val <= 100) {
        sum += val;
        ++val;
    }
    std::cout << "Sum of 50 to 100 inclusive is ";
    std::cout << sum << std::endl;
    return 0;
}
```
### 练习 1.10
>除了`++`运算符将运算对象的值增加1之外，还有一个递减运算符`--`实现将值减少1。编写程序，使用递减运算符在循环中按递减顺序打印出10到0之间的整数。
```c++
include <iostream>

int main()
{
    int val = 10;
    while (val <= 0) {
        std::cout << val << std::endl;
        --val;
    }
    retusrn 0;
}
```
### 练习 1.11
>编写程序，提示用户输入两个整数，打印出这两个整数所指定的范围内的所有整数。
```c++
include <iostream>

int main()
{
    int i = 0, j = 0;
    std::cin >> i >> j;
    while (i >= j) {
        std::cout << i << std::endl;
        --i;
    }
    return 0;
}
```
## 1.4.2 节练习
### 练习 1.12
>下面的for循环完成了什么功能？sum的值最终是多少？
```c++
int sum = 0;
for (int i = -100; i <= 100; ++i)
    sum += i;
```
### 练习 1.13
>使用for循环重做1.41节中的所有练习。
```c++
include <iostream>

int main()
{
    int sum = 0;
    for (int i = 50; i <= 100; i++)
        sum += i;
    std::cout << sum << std::endl;
    return 0;
}
```
```c++
include <iostream>

int main()
{
    for (int i = 10; i >= 0; --i)
        std::cout << i << std::endl;
    return 0;
}
```
```c++
include <iostream>

int main()
{
    int small = 0, large = 0;
    std::cout "Enter two integers from small to large:"
    std::cin >> small >> large;
    for (i = small; i <= large; ++i)
        std::cout << i << std::endl;
    return 0;
}
```
### 练习 1.14
>对比for循环和while循环，两种形式的优缺点各是什么？
### 练习 1.15
>编写程序，包含14页“再探编译”中讨论的常见错误。熟悉编译器生成的错误信息。
## 1.4.3 节练习
### 练习 1.16
>编写程序，从cin读取一组数据，输出其和。
```c++
include <iostream>

int main()
{
    int sum = 0, val = 0;
    while (std::cin >> val)
        sum += val;
    std::cout << sum << std::endl;
    return 0;
}
```
## 1.4.4
### 练习 1.17
>如果输入的所有值都是相等的，本节的程序会输出什么？如果没有重复值，输出又会是怎样的？
### 练习 1.18
>编译并运行本节的程序，给它输入全都相等的值。再次运行程序，输入没有重复的值。
### 练习 1.19
>修改你为练习1.11所编写的程序，使其能够处理用户输入的第一个数比第二个数小的情况。
```c++
include <iostream>

int main()
{
    int i = 0, j = 0;
    std::cin >> i >> j;
    if (i < j) {
        while (i <= j) {
            std::cout << i << std::endl;
            ++i;
        }
    }
    else {
        while (i >= j) {
            std::cout << i << std::endl;
            --i;
        }
    }
    return 0;
}
```
## 1.5.1 节练习
### 练习 1.20
>在网站[http://www.informit.com/title/0312714113](http://www.informit.com/title/0312714113)上，第1章的代码目录中包含了头文件[Sales_item.h](https://github.com/liwei1997/CppPrimerAnswer/blob/master/ch01/Sales_item.h)。将它拷贝刀你自己的工作目录中。用它编写一个程序，读取一组书记的销售记录，将每条记录打印到标准输出上。
```c++
#include <iostream>
#include "Sales_item.h"

int main()
{
    for (Sales_item books; std::cin >> books; std::cout << books << std::endl);
    return 0;
}
```
### 练习 1.21
>编写程序，读取两个ISBN相同的Sales_item对象，输出它们的和。
```c++
include <iostream>
include "Sales_item.h"

int main()
{
    Sales_item item1, item2;
    std
    if(item1.isbn()==item2.isbn)
}
```


