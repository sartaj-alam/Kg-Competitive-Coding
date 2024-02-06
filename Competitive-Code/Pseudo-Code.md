## 1. 
```c
 Int a = 1
 while(++a <=5)
    Print a++

// Output  2 4
```

## 2.
```c
Integer a=1, b=2
For(Integer i = 0; i<=6; i = i+2)
     a = a+b+i
     a = a+b
     b = a-b
     Print b
End For
// Ouput 3 10 27 70 
```

## 3.
```c
Integer n
For(n= 3; n!=0; n--)
Print n
n = n-1
end For

//Output Infinite Loop (3 1 -1 -3 -5 .......)
```
## 4.
```c
what will be the value of s if n = 127

Read n
i=0,s=0

Function Tesla(int n)
      
      while(n>0)
      r=n%10
      p=8^i
      s=s+p*r
      i++
      n=n/10
      End while
      Return s;
End Function
// Output 87
```

## 5.
```c
Read num1, num2, num3
if(num1 < num2)
  if(num2 <num3)
  Write num1, num2, num3
  else
  if(num3 < num1)
  Write num3, num1, num2
  else
  Write num1, num3, num2
else
 if(num1 < num3)
 Write num2, num1, num3
 else
 if(num3 < num2)
 Write num3, num2, num1
 else
 Write num2, num3, num1

//here Read and Write is for compiler not for us, so that oposite for us (Read means cin and Write means cout)

// Output is dispaly in Ascending order.
```

## 5.
```c
#include<stdio.h>

int main(){
    int a=10, b=20, c=30;
    if(c>b>a)
    printf("TRUE");
    else
    printf("FALSE");
return 0;
}

// Output is --->FALSE    (kyuki if execute right to left)
```