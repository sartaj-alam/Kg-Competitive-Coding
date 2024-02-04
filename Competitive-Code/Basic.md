// Whole Code is written in five language, C, C++, Java, Python, and JavaScript


## 1. Write a program to find the factorial of a number given by user.

#  C 
``` C
// Online C compiler to run C program online
#include <stdio.h>

unsigned int factorial (unsigned int n){
    int res = 1, i;
    for(i = 2; i <= n; i++)
        res = res * i;
    return res;
}

int main() {
    // Write C code here
    int num;
    scanf("%u", &num);
    printf("Factorial of %u is %u ", num, factorial(num));

    return 0;
}
```
#  C++ 
```C++
// Online C++ compiler to run C++ program online
#include <iostream>
using namespace std;
unsigned int factorial( unsigned int n){
    int res = 1, i;
    for(i = 2; i <= n; i++)
    res = res * i;
return res;
}

int main() {
    // Write C++ code here
    int num;
    cout<<"Enter a number ";
    cin>>num;
    cout << "Factorial of "<<num<<" is "<<factorial(num);

    return 0;
}
```

##  java

```java
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class HelloWorld {
    
     int factorial ( int n ){
        int res = 1, i = 2;
        while(i <= n){
        res = res * i;
        i++;
        }
    return res;
    }
    
    public static void main(String[] args) {
        HelloWorld H = new HelloWorld();
        System.out.println("Enter a number ");
        Scanner Sc = new Scanner(System.in);
        int num = Sc.nextInt();
        System.out.println("Facorial is " + H.factorial(num));
    }
}
```
## python
```python
def factorial (n):
    res =1
    i = 2;
    while(i <= n):
        res = res * i;
        i = i+1
    return res;

num = int(input("Enter a number "));
print("Factorial is ", factorial(num))
```

## 2. WAP to find the area of circle when diameter is given

```C
// Online C compiler to run C program online
#include <stdio.h>

float area(float diameter){
    float radi = (float) diameter/ 2;
    return (3.14 * radi * radi);
}

int main() {
    // Write C code here
    int num;
    scanf("%u", &num);
    printf("Area  is %.2f ", area(num) );

    return 0;
}
```
## C++
```C++
// Online C++ compiler to run C++ program online
#include <iostream>
#include<iomanip>
using namespace std;
float area( float diameter){
    float redi = diameter/ 2.0;
    
return (3.14  * redi * redi);
}

int main() {
    // Write C++ code here
    float num;
    cout<<"Enter a number ";
    cin>>num;
    cout << "Area  is "<<setprecision(2)<<area(num);

    return 0;
}
```
## java
```java
import java.util.Scanner;
class HelloWorld {
    
     float area ( float diameter ){
        float redi = (float)(diameter / 2.0);
    return (float)(3.14 * (redi * redi));
    }
    
    public static void main(String[] args) {
        HelloWorld H = new HelloWorld();
        System.out.println("Enter a number ");
        Scanner Sc = new Scanner(System.in);
        int num = Sc.nextInt();
        System.out.println("area is " + H.area(num));
    }
}
```

## 3. Wap to find the GCD(hcf) of two number
## C
```c
// Online C compiler to run C program online
#include <stdio.h>

int Gcd(int a , int b){
    if(a == 0){
        return b;
    }
    else if(b == 0){
        return a;
    }
    else if( a == b){
        return a;
    }
    else if( a > b){
        return Gcd(a-b , b);
    }
    else{
    return Gcd(a , b-a);
}
}
int main() {
    // Write C code here
    int num1 , num2;
    scanf("%u" , &num1);
    scanf("%u", &num2);
    printf("GCD  is %u ", Gcd(num1  , num2) );

    return 0;
}
```
## C++
```C++
// Online C compiler to run C program online
#include <iostream>
using namespace std;
int Gcd(int a , int b){
    if(a == 0){
        return b;
    }
    else if(b == 0){
        return a;
    }
    else if( a == b){
        return a;
    }
    else if( a > b){
        return Gcd(a-b , b);
    }
    else{
    return Gcd(a , b-a);
}
}
int main() {
    // Write C code here
    int num1 , num2;
    cin>>num1>>num2;
    
    cout<<"GCD  is  " <<Gcd(num1  , num2) ;

    return 0;
}
```
## 4.WAP to find number is prime or not, if number is prime then print the sqoure root of the number upto two decimal

## C
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <math.h>
int main() {
    // Write C code here
    int n, flag = 0 ;
    scanf("%u" , &n);
    for(int i = 2; i < n/2; i++){
        if(n % i == 0){
            flag = 1;
            break;
        }
    }
    if(flag == 1){
        printf("Number is not prime ");
    }
    else {
    printf("Number is prime %.2f", sqrt(n) );
    }

    return 0;
}
```
## C++
```C++
// Online C compiler to run C program online
#include <iostream>
#include<math.h>
using namespace std;

int main() {
    // Write C code here
    int n,flag = 0;
    cin>>n;
    for(int i = 2; i < n/2; i++){
        if(n % i == 0){
            flag = 1;
            break;
        }
    }
    if(flag == 1){
        cout<<"Number is not prime ";
    }
    else {
    cout<<"Number is prime "<< sqrt(n) ;
    }

    return 0;
}
```

## 5. wap to find the all possible prime number whithin a range
## c
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int findPrime(int n){
    if(n == 1)
    return 0;
    int i, flag = 0;
    for(i = 2; i < n; i++){
        if(n % i == 0){
            flag = 1;
            break;
        }
        
    }
    if(flag == 1)
    return 0;
    else return n;
}
int main() {
    // Write C code here
    int num1, num2 ;
    scanf("%u" , &num1);
    scanf("%u" , &num2);
    
    for(int i = num1; i <= num2; i++ )
    {
        if(findPrime(i)){
            printf("%u ", i);
        }
    }
    

    return 0;
}
```
## c++
```c++
// Online C compiler to run C program online
#include <iostream>
#include<math.h>
using namespace std;

int findPrime(int n){
    if(n == 1)
    return 0;
    int i, flag = 0;
    for(i = 2; i < n; i++){
        if(n % i == 0){
            flag = 1;
            break;
        }
        
    }
    if(flag == 1)
    return 0;
    else return n;
}
int main() {
    // Write C code here
    int num1, num2 ;
    cin>>num1>>num2;
    
    for(int i = num1; i <= num2; i++ )
    {
        if(findPrime(i)){
            cout<<" "<<i;
        }
    }
    

    return 0;
}
```

## 6. wap to find the sum of all posible prime number within a range

## C
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int findPrime(int n){
    if(n == 1)
    return 0;
    int i, flag = 0;
    for(i = 2; i < n; i++){
        if(n % i == 0){
            flag = 1;
            break;
        }
        
    }
    if(flag == 1)
    return 0;
    else return n;
}
int main() {
    // Write C code here
    int num1, num2, result = 0;
    scanf("%u" , &num1);
    scanf("%u" , &num2);
    
    for(int i = num1; i <= num2; i++ )
    {
        if(findPrime(i)){
            result = result + i;
        }
    }
    printf("Result %u", result);

    return 0;
}
```
## C++
```c++
// Online C compiler to run C program online
#include <iostream>
#include<math.h>
using namespace std;

int findPrime(int n){
    if(n == 1)
    return 0;
    int i, flag = 0;
    for(i = 2; i < n; i++){
        if(n % i == 0){
            flag = 1;
            break;
        }
        
    }
    if(flag == 1)
    return 0;
    else return n;
}
int main() {
    // Write C code here
    int num1, num2,result = 0 ;
    cin>>num1>>num2;
    
    for(int i = num1; i <= num2; i++ )
    {
        if(findPrime(i)){
            result = result + i;
        }
    }
    cout<<" Sum is "<< result;
    

    return 0;
}
```

## 7. wap to find the gretest number among three number (all number is not equal)
## C
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int a, b, c;
    scanf("%u", &a);
    scanf("%u", &b);
    scanf("%u", &c);
    if(a > b && a > c){
        printf("Greatest Number %u", a);
    }
    else if(b > a && b > c){
        printf("Greatest Number %u", b);
    }
    else {
        printf("Greatest Number %u", c);
    }

    return 0;
}
```
## c++
```c++
// Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
int main() {
     int a, b, c;
    cin>>a>>b>>c;
    if(a > b && a > c){
        cout<<"Greatest Number "<< a;
    }
    else if(b > a && b > c){
            cout<<"Greatest Number "<< b;
    }
    else {
     cout<<"Greatest Number "<< c;
    }
    return 0;
}
```
## java
```java
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class HelloWorld {
    public static void main(String[] args) {
        Scanner Sc = new Scanner(System.in);
        int a = Sc.nextInt();
        int b = Sc.nextInt();
        int c = Sc.nextInt();
        if(a > b && a > c){
             System.out.println("Greatest Number " + a);
    }
    else if(b > a && b > c){
                 System.out.println("Greatest Number " + b);
    }
    else {
     System.out.println("Greatest Number " + c);
    }
       
    }
}
```
## 8.wap to find smallest number among 4 number (number are not equal)
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int a, b, c,d;
    scanf("%u %u %u %u", &a, &b, &c, &d);
  
    if(a < b && a < c && a < d ){
        printf("Smallest Number %u", a);
    }
    else if(b < a && b < c && b < d){
        printf("Samllest Number %u", b);
    }
    else if( c < a && c < b && c < d){
        printf("Smallest Number %u", c);
    }
     else {
        printf("Smallest Number %u", d);
    }

    return 0;
}
```
## c++
```c++
// Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
int main() {
     int a, b, c,d;
    cin>>a>>b>>c>>d;
    if(a < b && a < c && a < d){
        cout<<"Smallest Number "<< a;
    }
    else if(b < a && b < c && b < d){
            cout<<"Smallest Number "<< b;
    }
    else if(c < a && c < b && c < d){
            cout<<"Smallest Number "<< c;
    }
    else {
     cout<<"Smallest Number "<< d;
    }
    return 0;
}
```
## java 
```java
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class HelloWorld {
    public static void main(String[] args) {
        Scanner Sc = new Scanner(System.in);
        int a = Sc.nextInt();
        int b = Sc.nextInt();
        int c = Sc.nextInt();
        int d = Sc.nextInt();
        if(a < b && a < c && a < d){
             System.out.println("Smallest Number " + a);
    }
    else if(b < a && b < c && b < d){
                 System.out.println("Smallest Number " + b);
    }
    else if(c < a && c < b && c < d){
                 System.out.println("Smallest Number " + c);
    }
    else {
     System.out.println("Smallest Number " + d);
    }
       
    }
}
```

## 9.wap to find second greatest number among 3 number(number is not same)
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int a, b, c;
    scanf("%u %u %u", &a, &b, &c);
  
    if(a > b && a > c ){
        if(b > c)
        printf("Greatest Number %u", b);
        else
        printf("Greatest Number %u", c);
    }
    else if(b > a && b > c ){
        if(a > c)
        printf("Greatest Number %u", a);
        else
        printf("Greatest Number %u", c);
    }
    else if(c > a && c > b){
        if(a > b)
        printf("Greatest Number %u", a);
        else
        printf("Greatest Number %u", b);
    }

    return 0;
}
```
## c++
```c++
// Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
int main() {
     int a, b, c;
    cin>>a>>b>>c;
    if(a > b && a > c){
        if(b > c )
        cout<<"Greatest Number "<< b;
        else
        cout<<"Greatest Number "<< c;
    }
    else if(b > a && b > c){
        if(a > c )
        cout<<"Greatest Number "<< a;
        else
        cout<<"Greatest Number "<< c;
    } 
    else if(c > a && c > b){
        if(a > b )
        cout<<"Greatest Number "<< a;
        else
        cout<<"Greatest Number "<< b;
    }
    return 0;
}
```
## java
```java
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class HelloWorld {
    public static void main(String[] args) {
        Scanner Sc = new Scanner(System.in);
        int a = Sc.nextInt();
        int b = Sc.nextInt();
        int c = Sc.nextInt();
        if(a > b && a > c){
            if(b > c)
             System.out.println("greatest Number " + b);
             else
             System.out.println("greatest Number " + c);
    }
    else  if(b > a && b > c){
            if(a > c)
             System.out.println("greatest Number " + a);
             else
             System.out.println("greatest Number " + c);
    }
    else  if(c > b && c > a){
            if(b > a)
             System.out.println("greatest Number " + b);
             else
             System.out.println("greatest Number " + a);
    }
       
    }
}
```

## 10. wap to user enter dd-mm-yyyy find out the numbers of days in month ( ignore leap year)
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int a, b, c;
    scanf("%u %u %u", &a, &b, &c);
  
    if(b == 1 || b == 3 || b == 5 || b == 7 || b == 8 || b == 10 || b == 31 ){
        printf("31");
    }
    else  if(b == 4 || b == 6 || b == 9 || b == 11 ){
        printf("30");
    }
    else if(b == 2)
    printf("28");

    return 0;
}
```
## c++
```c++
// Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
int main() {
     int a, b, c;
    cin>>a>>b>>c;
    if(b == 1 || b == 3 || b == 5 || b == 7 || b == 8 || b == 10 || b == 31 ){
        cout<<"31";
    }
    else  if(b == 4 || b == 6 || b == 9 || b == 11 ){
       cout<<"30";
    }
    else if(b == 2)
   cout<<"28";
    return 0;
}
```
## java
```java
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class HelloWorld {
    public static void main(String[] args) {
        Scanner Sc = new Scanner(System.in);
        int a = Sc.nextInt();
        int b = Sc.nextInt();
        int c = Sc.nextInt();
         if(b == 1 || b == 3 || b == 5 || b == 7 || b == 8 || b == 10 || b == 31 )
         {
             System.out.println("31");
         }
    
    else  if(b == 4 || b == 6 || b == 9 || b == 11 ){
       System.out.println("30");
    }
    else  if(b == 2){
        System.out.println("28");
    }
       
    }
}
```

## 11. wap to find whether the number is perfect square or not
## c
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int main() {
    // Write C code here
    int a;
    scanf("%u", &a);
    int b = sqrt(a);
    if(a == (b * b))
    printf("Success");
    else
    printf("Failure");
    return 0;
}
```
## c++
```c++
// Online C compiler to run C program online
#include <iostream>
#include <math.h>

using namespace std;
int main() {
    // Write C code here
    int a;
    cin>>a;
    int b = sqrt(a);
    if(a == (b * b))
    cout<<"Success";
    else
    cout<<"Failure";
    return 0;
}
```
## 12.wap to find sum of digit
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int a, b = 0;
    scanf("%u", &a);
    while(a){
        b = b + (a % 10);
        a = a / 10;
    }
    printf("%u",b);
    
    return 0;
}
```
## C++
```c++
// Online C compiler to run C program online
#include <stdio.h>
#include <iostream>

using namespace std;
int main() {
    // Write C code here
    int a, b = 0;
    cin>>a;
    while(a){
        b = b + (a % 10);
        a = a / 10;
    }
    cout<<b;
    
    return 0;
}
```
## java
```java
// Online Java Compiler
// Use this editor to write, compile and run your Java code online
import java.util.Scanner;
class HelloWorld {
    public static void main(String[] args) {
        Scanner Sc = new Scanner(System.in);
        int a = Sc.nextInt();
        int sum =0;
        while(a != 0){
            sum = sum + (a % 10);
            a = a / 10;
        }
        System.out.println(sum);
       
    }
}
```  
## 13.wap to print the digits of given number in same order.
## c (our concept)
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    unsigned int a,dup, div = 1,count = 0;
    scanf("%u", &a);
    dup = a;
    while(dup){
        count ++;
        dup = dup / 10;
        div = div * 10;
    }
    div = div / 10;
    while(count){
        dup = a / div;
        a = a % div;
        div = div / 10;
        count --;
        printf("%u ", dup);
    }
    

    return 0;
}
```
## c (Yash sir using array concept)
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    unsigned int num, arr[10];
    int i = 0, j, r;
    
    scanf("%u", & num);
    while(num){
        r = num % 10;
        arr[i] = r;
        i++;
        num = num / 10;
    }
    j = i - 1;
    while(j > -1){
        printf("%u ", arr[j]);
        j--;
    }
    

    return 0;
}
```
## C++ ( Our concept)
```c++
// Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
int main() {
    // Write C++ code here
    unsigned int num, dup, count = 0, div = 1;
    cin>>num;
    dup = num;
    
    while(dup){
        count ++;
        dup = dup / 10;
        div = div * 10;
    }
    div = div / 10;
    
    while(count){
        dup = num / div;
        num = num % div;
        div = div / 10;
        count --;
        cout<<dup<<" ";
    }

    return 0;
}
```

## 14. wap to print box number pattern of 1 and 0.
 <!-- 
 input: 5 5 
 output:
 1 1 1 1 1
 1 0 0 0 1
 1 0 0 0 1
 1 0 0 0 1
 1 1 1 1 1
  -->
## C
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    unsigned int row, col;
    
    scanf("%u %u", &row, &col);
    
    for(int i = 0; i < row; i++){
        
        for( int j = 0; j < col; j ++){
            
            if(i == 0 || i == row  -1 ){
                printf("1 ");
            }
            else if((i >= 1 && j == 0) || ( i >= 1 && j == col -1)){
                printf("1 ");
            }
            else {
                printf("0 ");
            }
        }
        printf("\n");
    }
    
    

    return 0;
}
```

## 15.wap to check the existing pair with given sum in array(Q16 is also Q15)
<!-- 
Dynamic programming concept is using here
example 1
 Sum = 10;
 No. of Array elements = 9
 Array Element = 0 2 5 7 4 6 10 20 -10
 
 output
 Array has two element with given sum

 example2
 Sum = 4
 No.of Array elements = 3
 Array element = 1 4 6

 output
 Sorry there is no any pair
 -->
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <stdlib.h>

int main() {
    // Write C code here
    int n, i, j, *ptr, sum, flag = 1;
    printf("Enter Sum : ");
    scanf("%d", &sum);
    
    printf("Enter number of Element : ");
    scanf("%d", &n);
    
    ptr = (int*) malloc(n * sizeof(int));
    
    if(ptr == NULL){
        printf("Error! memory is not located ");
        exit(0);
    }
    
    printf("Enter Element ");
    for(i = 0; i < n; ++i){
        scanf("%d", ptr + 1);
    }
    
   for( i = 0; i < n; i++){
       
       for(j = i; j < n; j++){
           if((ptr[i] + ptr[j]) == sum){
               printf("Array has two element ");
               flag = 0;
               break;
           }
       }
       if(!flag){
           break;
       }
   }
   if(flag){
       printf("Sorry Array does not have any two element");
   }
    
    free(ptr);
    

    return 0;
}
 ```
 ## 17.wap to print below pattern
 <!-- 
 input = 4
 output
 1
 2*2
 3*3*3
 4*4*4*4
 4*4*4*4
 3*3*3
 2*2
 1
  -->
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int num;
    scanf("%d", &num);
    for(int i = 1; i <= num; i++){
        
        for(int j = 1; j <= i; j++){
            if(j == i)
            printf("%u", i);
            else
            printf("%u * ", i);
        }
        printf("\n");
    }
    for(int i = num; i >0; i--){
        
        for(int j = i; j > 0; j--){
            if(j == 1)
            printf("%u", i);
            else
            printf("%u * ", i);
        }
        printf("\n");
    }

    return 0;
}
```
## 18. wap to check whether the number is plus perfect(amstrong number) or not (Q19 is same Q18)
## c
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int main() {
    // Write C code here
    int num,dup, sum = 0, p= 0;
    scanf("%d", &num);
    
    dup = num;
    while(dup){
        p ++;
        dup = dup / 10;
    }
    dup = num;
    while(dup){
        int remind = dup % 10;
        sum = sum + pow(remind, p);
        dup = dup / 10;
    }
    
    if(sum == num){
        printf("Yes It is  plus perfect number %u", num);
    }
    else {
        printf("Sorry! It is not plus perfect number %u", num);
    }
    

    return 0;
}
```
## C++
```c++
// Online C++ compiler to run C++ program online
#include <iostream>
#include <math.h>

using namespace std;
int main() {
    // Write C++ code here
    int num, dup, sum = 0, p = 0;
    cin>>num;
    
    dup = num;
    while(dup){
        p++;
        dup = dup / 10;
    }
    
    dup = num;
    while(dup){
        int remind = dup % 10;
        sum = sum + pow(remind, p);
        dup = dup / 10;
    }
    
    if(sum == num)
    cout << "Yes It is plus perfect number "<< num;
    else
    cout<<"Sorry It is not plus perfect number"<< num;

    return 0;
}
```
## 20.wap for given sorted array with many duplicate elements, the problem is to find the indexes of first and last occurance of an element x in given array. start the array from 0 index. if element x is not present in the array, print "No Occurance"

## c
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <stdlib.h>


void findFirstAndLast(int arr[], int n, int x){
    int first = -1, last = -1;
    for(int i = 0; i < n; i++){
        
        if(x != arr[i])
            continue;
        if(first == -1)
            first = i;
        last = i;
    }
    if(first != -1){
       printf("No Occurance");
    }
    else{
         printf("%d %d", first, last);
    }
}

int main() {
    // Write C code here
 
    int n, x, *ptr;
    printf("Enter number of element ");
    scanf("%d", &n);
    ptr = (int*) malloc (n * sizeof(int));
    
    if(ptr == NULL){
        printf("Error! memory is not allocated");
        exit(0);
    }
    
    printf("Enter Element ");
    for(int i = 0; i < n; ++i){
        scanf("%d", ptr + 1);
    }
    
    printf("Enter number to be searched ");
    scanf("%d", &x);
    findFirstAndLast(ptr, n, x);
   
    

    return 0;
}
```