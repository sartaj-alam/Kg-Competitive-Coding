## From Intermediate section and Q24
## 24.Example to identify the pattern
<!-- 
 Input         Output
 10             5
 15             8
 23             12
 99             50
 107            54
 -->
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int num, x;
    printf("Enter the number : ");
    scanf("%d", &num);
    
    
    x = num / 2;
    if(num % 2 == 0)
    printf("%d", x);
    else
    printf("%d", x+1);
    

    return 0;
}
 ```

## 25. If Ajay Devagn makes a vimal packets in 'x' days, Sharddha makes the same vimal packet in 'y' days and Deepika makes same vimal packets in 'z' days. You need to writes a program where the inputs x, y,z are taken from user and the output is the number of days it will take to make vimal packet if all three work together.
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int  x, y, z;
    printf("Enter the number of days for Ajay : ");
    scanf("%d", &x);
    printf("Enter the number of days for Sharddha : ");
    scanf("%d", &y);
    printf("Enter the number of days for Deepika : ");
    scanf("%d", &z);
    
    unsigned int total = x * y *z;
    x = total / x;
    y = total / y;
    z = total / z;
    printf("%f", ((total) / (x+y+z)));
    

    return 0;
}
```

## 26 Given a series of numbers 2, 10, 30, 68, 130..., identify the pattern in the series and help to identify the integer at other indices. Indices are starting from 1.(logic is a^3+a )
## c
```c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int  x;
    printf("Enter the number of series : ");
    scanf("%d", &x);
    printf("Series is : ");
    for(int i = 1; i <= x; i++){
        printf("%d ", ((i*i*i) + i));
    }
    

    return 0;
}
```

## 28. Jetha lal has a kangaru Binod. Binod is very hungry and jetha decides to feed it by playing a little game. Binod is a special kangaroo which can jump as far  as it wants but has a special pattern. He start at the point 0. In his turn, he can make a jump of 1 unit. Now for all consequent turns, if the kangaroo is currently at a distance x (from the start), his jump will take him x units forword. Givena leaf at a distance N, you have to find if the kangaroo can reach that leaf or not.
## c
```c
// Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int main() {
    // Write C code here
    int  x, intvar;
    printf("Enter the number : ");
    scanf("%d", &x);
    double floatvar = log2((double)x);
    intvar = floatvar;
    if(intvar == floatvar)
    printf("True");
    else 
    printf("False");
    

    return 0;
}
```
