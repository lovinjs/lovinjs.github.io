---
title: a + b
date: 2017-10-11 18:24:42
categories: ACM
tags: [acm,algorithm]
---
![ACM](/images/acm.png)

ACM入门问题之a+b，即输入两个整数a和b，输出a+b的值

<!-- more -->

#### 题目1：
原题地址：[HDOJ_1089](http://acm.hdu.edu.cn/showproblem.php?pid=1089)

示例：
```
Input:
1  5
10  20

Output:
6
30
```

>题目无具体的输入数据组数说明，因此需要自己加以判断
>scanf函数返回值为int型，大小是成功输入的合格参数的个数，成功一个返回1，二个返回2，没有返回-1

代码：
```c
#include<stdio.h>
int main()
{
    int a,b;
    while(scanf("%d%d",&a,&b)==2)  //或者把“==2”改为“!=EOF”，EOF是一个预定义常量，等于-1
        printf("%d\n",a + b );
    return 0;
}
```

#### 题目2
原题地址：[HDOJ_1090](http://acm.hdu.edu.cn/showproblem.php?pid=1090)

示例：
```
Input:
2
1  5
10  20

Output:
6
30
```

>题目一开始就说明了具体的输入数据组数，第一行说明了有N组数据，例如此题有2组输入数据

代码：
```c
#include<stdio.h>
int main()
{
    int N,i,a,b;
    scanf("%d",&N);
    for(i=0;i<N;i++)    //利用for循环控制输入次数
    {
        scanf("%d%d",&a,&b);
        printf("%d\n",a + b );
    }
    return 0;
}
```

#### 题目3
原题地址：[HDOJ_1091](http://acm.hdu.edu.cn/showproblem.php?pid=1091)

示例：
```
Input:
1  5
10  20
0  0

Output:
6
30
```

>题目没有说明具体的输入组数，但是以特殊输入作为结束标志

代码：
```c
#include<stdio.h>
int main()
{
    int a,b;
    while(scanf("%d%d",&a,&b)==2&&(a!=0||b!=0))  //判断是否是特殊输入
    printf("%d\n",a+b);
    return 0;
}
```

#### 题目4（综合练习）
原题地址：[HDOJ_1092](http://acm.hdu.edu.cn/showproblem.php?pid=1092)

示例：
```
Input:
4 1 2 3 4
5 1 2 3 4 5
0

Output:
10
15
```

>此题是对1~3道题目的综合练习

代码：
```c
#include<stdio.h>
int main()
{
    int N,i,a,sum;
    while(scanf("%d",&N)&&N){  //先判断第一个输入的数是否合理
        sum=0;
        for(i=0;i<N;i++){      //利用for循环控制次数
            scanf("%d",&a);
            sum+=a;
        }
        printf("%d\n",sum);
    }
    return 0;
}
```

#### 题目5（综合练习）
原题地址：[HDOJ_1093](http://acm.hdu.edu.cn/showproblem.php?pid=1093)

示例：
```
Input:
2
4 1 2 3 4
5 1 2 3 4 5

Output:
10
15

```

>此题是对1~4道题目的综合练习

代码：
```c
#include<stdio.h>
int main()
{
    int N,M,i,j,a,sum;
    scanf("%d",&N);
    for(i=0;i<N;i++){   //控制输入组数
        while(scanf("%d",&M)){
            sum=0;
            for(j=0;j<M;j++){
                scanf("%d",&a);
                sum+=a;
            }
            printf("%d\n",sum);
            break;  //此处需要跳出循环，否则死循环
        }
    }
    return 0;
}
```

#### 题目6（综合练习）
原题地址：[HDOJ_1094](http://acm.hdu.edu.cn/showproblem.php?pid=1094)

示例：
```
Input:
4 1 2 3 4
5 1 2 3 4 5

Output:
10
15

```

>此题是对1~5道题目的综合练习

代码：
```c
#include<stdio.h>
int main()
{
    int N,i,a,sum;
    while(scanf("%d",&N)!=EOF&&N){  //这里不判断N是否>0也是可以ac的
        sum=0;
        for(i=0;i<N;i++){
            scanf("%d",&a);
            sum+=a;
        }
        printf("%d\n",sum);
    }
    return 0;
}
```
