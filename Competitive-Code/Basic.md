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