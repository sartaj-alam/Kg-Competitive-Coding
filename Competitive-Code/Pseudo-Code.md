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
## 6
```c
What will be the output of the following pseudo code

Integer x,y,z
Set x = 24, y=8
x = x/y
z = y<<x
Print z

// Output is 64 (For left shift  a<<b ----> a*2^b, so  8*2^3)
```

## 7
```c
Find the output of the following pseudo code 

Integer value, n

Set value = 1, n = 45

while(value less than equal to n)
value = value<<1
End loop
Print value

// Output is 64
```

## 8
```c
Find the output of the following pseudo code 

Integer count, i

Set count = 0,i = 0
for i to 4<<0
count = count + i
end loop
Print count

//  Output is 10   (line 129 ----> for(i= 0; i<=4; i++))
```

## 9
```
What will be the output of the following pseudo code 

Integer x, y, z, a
Set x= 2, y=1, z=5
a = (x AND y) OR (z+1)
print a

Output
A)    5
B)    3
C)    2
D)    1

// Output is option D.
```

## 10
```c
What will be the output of the following pseudo code 

Integer a

String str1
Set str1 = "booty"

 a= stringLength(str1)

 Print(a^1)

 Option
 A)    0
 B)    4
 C)    5
 D)    3

 // Output is option B   ( a^1 ---> means a xor 1 (xor ---> 00-->0, 10-->1, 01-->1, 11-->0))
 // 5 ---> 101 , 1---> 001,  101 XOR 001 ---> 100, 100---> means 4
```

## 11
```c
What will be the output of the following pseudo code
Read x
Set sum to 0;

while(x >= 0)
   Set sum to x + sum
   Read x
End while
Write sum

// Output is sum of all positive integer including 0, and whenever user give negative number program will stop and print sum of all positive number
```

## 12
```c
What will be the output of following pseudo code

Read count
Set x to 0;
while(x < count)
   Set even to even + 2
   x = x + 1
End while
Write even

// Output is 2 times count, (initially even = 0 and loop run count times and count = count + 2)
```