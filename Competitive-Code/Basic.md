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
## 3.WAP to find number is prime or not, if number is prime then print the sqoure root of the number upto two decimal

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

## 4. wap to find the all possible prime number whithin a range
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

## 5. wap to find the sum of all posible prime number within a range

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