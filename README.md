# C-question-record

## 第四章   
    题目18.三个字符排序。空格隔开，从小到大。输出也用空格隔开。  
        1.输入：当输入三个字符时，最后的\n会被缓存，下一次会被读入，从而影响输入；  
        解决：%*c 或getchar() 二者均可，目的是消除\n  
        2.算法：三元运算一般比if更加耗内存；我采用的max，min，mid其实是一种笨方法，没有考虑三个元素之间的关系。把简单问题给复杂化了
        解决：采用if语句以及temp进行两两对换，最大值取出后，剩余两个进行一次比较即可得到最小值和中间值。
        使 a<=b<=c,分步就是：  
  ```C
   a<=b  
   a<=c  
   b<=c  
 ```  

## 第五章
    题目12 用递归实现任意正整数向八进制的转换
    问题：陷入一个误区，以为凡是递归必须要“return”。实际上递归只要直接或间接调用自身函数即可，“return”不是必须的。       方案：有这个误区是因为大多数递归需要return而已。

## 第七章  
    题目：程序7-5统计单词个数
      1.问题：将简单问题复杂化，或者说题目的描述不清楚，存在歧义
      2.算法 ：for(i = 0; str[i] != '\0' ; i++)
                    d = d * 2 + (str[i] - '0');
  这两行可以说是精髓，这个转换太巧妙了，应用了秦九韶算法

    题目：下面的字符串逆置函数更巧妙
  ```C
  char *strrev(char *str)
  {
    char *p1, *p2;  
    
    if (! str || ! *str)
        return str;

        for (p1 = str, p2 = str + strlen(str) - 1; p2 > p1; ++p1, --p2)
            {
                *p1 ^= *p2;
                *p2 ^= *p1;
                *p1 ^= *p2;
            }

        return str;
 }
```

## 第八章  
    题目：课后作业9 在一个字符串中删除一个字符
    homeword_test.c的方法更好，以后做完一道题，最好都要上网上找找答案

## 待做：  
    1.vim 再完整学一下
    2. 写以及计算编了多少程序的程序
    3.写几段程序运行时间，和占用内存的程序。搞懂判题系统是如何得出内存和运行时间的。
    4.第二遍看的时候，先在脑子里想一下，看能不“很快”想出来。不能的再留心一下。
           
