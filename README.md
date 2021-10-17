# 21
4.#include <stdio.h>
int main()
{                                                      
    int a, b, c;
    scanf_s("%d%d%d", &a, &b, &c);
    if (a < b)
a = b;
    if (a < c)
a = c;
    printf("%d\n", a);
    return 0;
}

改正后的   
#include <stdio.h>
int main()
{
    int a, b, c, d;
    scanf_s("%d%d%d", &a, &b, &c);
    if (a > b)d = a;
    else d = b;
    if (d > c) d =d;
    else d = c;
    printf("%d\n", d);
    return 0;
}
6.#include <stdio.h>
int main()
{
    float x,y;
    scanf_s("%f", &x);

    if (x >= 10){ y=3*x-11; }
    else if (x < 1) { y = x; }
    else if (x >= 1 && x < 10){  y = 2 * x - 1;}
   
  
    printf("%f\n", y);

}
8.1
#include <stdio.h>
int main()
{
    float x;
    scanf_s("%f", &x);
    if (x >= 90) {printf("‘A'");}
    if (x >=80 &&x < 90) { printf("‘B'"); }
    if (x >= 70 && x < 80) { printf("‘C'"); }
    if (x >= 60 && x < 70) { printf("‘D'"); }
    if (x >= 0 && x < 60) { printf("‘E'"); }
    return 0;

}
8.2
#include <stdio.h>
int main()
{
    int x,y;
    scanf_s("%d", &x);
    y=x/10;
    switch (y)
    { case 10:
      case 9:printf("‘A'");break;
      case 8:printf("‘B'"); break;
      case 7:printf("‘C'"); break;
      case 6:printf("‘D'"); break;
      case 5:
      case 4:
      case 3:
      case 2:
      case 1:
      case 0:printf("‘E'"); break;
      default:printf("enter date error !\n"); break;
    }
    return 0;

}
10.1
#include <stdio.h>
int main()
{
    float i,a;
    scanf_s("%f", &i);
    
    if (i <=100000)a=i*0.1;
    else a=100000*0.1;
    
    if (i>100000 && i <= 200000)a = (200000-i) * 0.075+ 100000 * 0.1;

    
     if (i > 200000 && i <= 400000)a = (i-200000) * 0.05+100000*0.075+ 100000 * 0.1;
   
    
     if (i > 400000 && i <= 600000)a = (i-400000) * 0.03+200000*0.05+ 100000 * 0.075 + 100000 * 0.1;
   
    
     if (i > 600000 && i <= 1000000)a = (i - 600000) * 0.015+200000*0.03+ 200000 * 0.05 + 100000 * 0.075 + 100000 * 0.1;

    
     if (i > 1000000) a = (i - 1000000) * 0.1+400000*0.015+200000 * 0.03 + 200000 * 0.05 + 100000 * 0.075 + 100000 * 0.1;


    printf("%f\n", a);
    return 0;
}
10.2
#include <stdio.h>
int main()
{
    int i,h;
    float a=0;
    
    scanf_s("%d", &i);
  
    if (i > 1000000)
	{h= 10;}
	else
	{h = i / 100000;}
     switch (h)
    { case 0:
      case 1:a=i*0.1;break;
      case 2:a=(200000 - i) * 0.075 + 100000 * 0.1; break;
      case 3:
      case 4:a= (i - 200000) * 0.05 + 100000 * 0.075 + 100000 * 0.1; break;
      case 5:
      case 6:a=(i - 400000) * 0.03 + 200000 * 0.05 + 100000 * 0.075 + 100000 * 0.1; break;
      case 7:
      case 8:
      case 9:a= (i - 600000) * 0.015 + 200000 * 0.03 + 200000 * 0.05 + 100000 * 0.075 + 100000 * 0.1; break;
      case 10:a=(i - 1000000) * 0.01 + 400000 * 0.015 + 200000 * 0.03 + 200000 * 0.05 + 100000 * 0.075 + 100000 * 0.1; break;
      default:printf("enter date error!\n"); }
    printf("利润 = %f\n", a);
    return 0;
}

9.
#include<stdio.h>
int main()
{
	int a, c, d, b, q, w;
	scanf_s("%d", &a);
	w = (a / 10000);
	q = (a % 10000) / 1000;
	b = (a % 1000) / 100;
	d = (a % 100) / 10;
	c = (a % 10);
	if (w >= 1)
	{
		printf("数的位数是5\n逆序输出为%d%d%d%d%d\n", c, d, b, q, w);
	}
	if (w < 1 && q >= 1)
	{
		printf("数的位数是4\n逆序输出为%d%d%d%d\n", c, d, b, q);
	}
	if (q < 1 && b >= 1)
	{
		printf("数的位数是3\n逆序输出为%d%d%d\n", c, d, b);
	}
	if (b < 1 && d>= 1)
	{
		printf("数的位数是2\n逆序输出为%d%d\n", c, d);
	}
	if (d < 1 && c>= 1)
	{
		printf("数的位数是1\n逆序输出为%d\n", c);
	}
	printf("每一位数字为%d,%d,%d,%d,%d\n", w, q, b, d, c);
	return 0;
