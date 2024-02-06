## 1.wap to print the count set of bits in given number
<!-- 
input
N = 6
output = 2
exaplanation 
binary 6  =====> 110
So the count of the set bits is 2

input
N = 6
output
1
expalanation
 binary 8 ====> 1000
 so the count of the set bit is 1
 -->
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int num, count = 0;
    printf("Enter Number : ");
    scanf("%d", & num);
    while(num){
        if(num % 2 == 1){
            count ++;
        }
        num = num / 2;
    }
    printf("Result : %d", count);

    return 0;
}
 ```
 ## C++
 ```c++
 // Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
int main() {
  int num, count = 0;
    cout<<"Enter Number : ";
    cin>> num;
    while(num){
        if(num % 2 == 1){
            count ++;
        }
        num = num / 2;
    }
    cout<<"Result :"<< count;
    return 0;
}
 ```
 ## 2.wap to display the factorial of any number(Q3 same as Q2)
 ## c (using recursion)
 ```c
 // Online C compiler to run C program online
#include <stdio.h>


unsigned int factorial (int n){
    
    if(n == 1){
        return 1;
    }
    return n * factorial(n-1);
}
int main() {
    // Write C code here
    unsigned int num, fact = 1;
    printf("Enter Number : ");
    scanf("%d", & num);
    if(num <= 0)
    printf("Factorial of %u is : %u", num , fact);
    else{
     fact = factorial(num);
     printf("Factorial of %u is : %u", num, fact);
    }
    

    return 0;
}
 ```
 ## c++ (using recursion)
 ```c++
 // Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
unsigned int factorial (int n){
    
    if(n == 1){
        return 1;
    }
    return n * factorial(n-1);
}
int main() {
    // Write C code here
    unsigned int num, fact = 1;
    cout<<"Enter Number : ";
    cin>>num;
    if(num <= 0)
    cout<<"Factorial of "<< num<<" is : " << fact;
    else{
     fact = factorial(num);
     cout<<"Factorial of "<< num<<" is : " << fact;
    }
    

    return 0;
}
 ```
 ## 4.wap find the middle of the given linked list
 ## c(yash sir)
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <stdlib.h>
 
 
 struct Node{
     
     int data;
     struct Node* next;
 };
 
 void printMiddle( struct Node *head){
     
     struct Node *slow_ptr = head;
     struct Node *fast_ptr = head;
     
     if(head != NULL){
         
         while(fast_ptr != NULL && fast_ptr -> next != NULL){
             
             fast_ptr = fast_ptr -> next ->next;
             slow_ptr = slow_ptr -> next;
         }
         printf("The Middle Element is : [%d]\n\n", slow_ptr -> data);
     }
     else {
         printf("Empty LinkedList....");
     }
 }
 
void push(struct Node** head_ref, int new_data){
    
    struct Node* new_node = (struct Node*) malloc (sizeof(struct Node));
    
    new_node -> data = new_data;
    new_node -> next = (*head_ref);
    (*head_ref) = new_node;
}

void printList( struct Node *ptr){
    
    while(ptr != NULL){
        printf("%d : %d ->  ",ptr ->  data, ptr -> next);
        ptr = ptr->next;
    }
    printf("NULL\n");
}

int main() {
   
   struct Node* head = NULL;
   int i;
   
   for(i = 5; i > 0; i--){
       
       push(&head, i);
       
   }
   printList(head);
    printMiddle(head);
   
    return 0;
}
 ```
 ## c(own concept but output is wrong)
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <stdlib.h>
 
 
 struct Node{
     
     int data;
     struct Node* next;
 };
 
 void printMiddle( struct Node *head){
     
     struct Node *slow_ptr = head;
     struct Node *fast_ptr = head;
     
     if(head != NULL){
         
         while(fast_ptr != NULL && fast_ptr -> next != NULL){
             
             fast_ptr = fast_ptr -> next ->next;
             slow_ptr = slow_ptr -> next;
         }
         printf("The Middle Element is : [%d]\n\n", slow_ptr -> data);
     }
     else {
         printf("Empty LinkedList....");
     }
 }
 
void linkedListMake(struct Node** head_ref, int new_data){
    
    struct Node* new_node = (struct Node*) malloc (sizeof(struct Node));
    
    new_node -> data = new_data;
    new_node -> next = (*head_ref);
    (*head_ref) = new_node;
}

void push()
{
    
     struct Node* head = NULL;
    int i, data;
    printf("Enter Length of the LinkedList : ");
    scanf("%d", &i);
   
    while(i){
        
        printf("Enter Data of the LinkedList : ");
        scanf("%d", &data);
        linkedListMake(&head, i);
         i--;
        
    }
}
void printList( struct Node *ptr){
    
    while(ptr != NULL){
        printf("%d : %d ->  ",ptr ->  data, ptr -> next);
        ptr = ptr->next;
    }
    printf("NULL\n");
}

int main() {
   
   struct Node* head = NULL;
   push();
   printList(head);
    printMiddle(head);
   
    return 0;
}
 ```
 ## 7.wap a function to return position of first 1 from right to left, in binary representation of an integer
 ## c++
 ```c++
 // Online C compiler to run C program online
#include <stdio.h>


void findIndex(int num){
    int count = 1;
  
    while(num){
        if(num % 2 == 1){
            printf("Index is : %d ", count);
            break;
        }
        count++;
        num = num / 2;
}
}
int main() {
    // Write C code here
    int num;
      printf("Enter Number : ");
    scanf("%d",&num);
    findIndex(num);


    return 0;
}
 ```
 ## c++
 ```c++
 // Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
void findIndex(int num){
    int count = 1;
  
    while(num){
        if(num % 2 == 1){
            cout<<"Index is :  "<< count;
            break;
        }
        count++;
        num = num / 2;
}
}
int main() {
    // Write C code here
    int num;
      cout<<"Enter Number : ";
    cin>>num;
    findIndex(num);


    return 0;
}
 ```

 ## 8.wap to take two input and find the position of rightmost different bit in binary representation of number

 ## c++
 ```c++
 // Online C compiler to run C program online
#include <stdio.h>

void findIndex(int num1, int num2){
   
     int count = 1, flag = 0;
     if(num2 < num1){
         int temp = num1;
         num1 = num2;
         num2 = temp;
     }
  
    while(num1){
        if((num1 % 2) != (num2 % 2) ){
            printf("Index is :  %d ", count);
            flag = 1;
            break;
        }
        count++;
        num1 = num1 / 2;
        num2 = num2 / 2;
}
  if(!flag)
  printf(" Index is : %d", count+1);
}
int main() {
    // Write C code here
    int num1, num2;
      printf("Enter Number : ");
    scanf("%d", &num1);
    scanf("%d", &num2);
    findIndex(num1, num2);


    return 0;
}
 ```
 ## c++
 ```c++
 // Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;
void findIndex(int num1, int num2){
   
     int count = 1, flag = 0;
     if(num2 < num1){
         int temp = num1;
         num1 = num2;
         num2 = temp;
     }
  
    while(num1){
        if((num1 % 2) != (num2 % 2) ){
            cout<<"Index is : "<< count;
            flag = 1;
            break;
        }
        count++;
        num1 = num1 / 2;
        num2 = num2 / 2;
}
  if(!flag)
  cout<<" Index is : "<< count+1;
}
int main() {
    // Write C code here
    int num1, num2;
      cout<<"Enter Number : ";
    cin>>num1;
    cin>>num2;
    findIndex(num1, num2);


    return 0;
}
 ```

 ## 9.wap to find the reminder when num1 is divided by num2
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int num1, num2;
    
    printf("Enter Numbers : ");
    scanf("%d %d", num1, num2);
    printf("%d", num1 % num2);

    return 0;
}
 ```
 ## c++
 ```c++
 // Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;

int main() {
    // Write C code here
    int num1, num2;
    
    cout<<"Enter Numbers : ";
    cin>> num1>> num2;
    cout<<"Result is : "<< num1 % num2;

    return 0;
}
 ```

 ## 10. Jetha like chocolates and he loves to try different ones. There are N shops in the market labelled from 1 to N and each shop offers a different variety of chocolate. Jetha started from ith shop and goes ahead to each and every shop. But as there are too many shops jhetha would like to know how many more shops he has visit. You have been given L denoting numbers of bits reuired to represent N. You need to return the maximum numbers of shops he can visit.
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int main() {
    // Write C code here
    int i, l;
    printf("Enter current position of shop : ");
    scanf("%d",&i);
    printf("Enter number of shop : ");
    scanf("%d", &l);
    int result = pow(2,l) - i;
    printf("%d", result);

    return 0;
}
 ```

 ## 11. wap to check whether year is leap year or not
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <math.h>

int main() {
    // Write C code here
    int year ;
    printf("Enter year : ");
    scanf("%d",&year);
    
    if(year % 100 == 0){
        
        if(year % 400 == 0)
        printf("Yes This is leap year. ");
        else
        printf("Sorry! This is not leap year. ");
    }
    else if(year % 4 == 0)
    printf("Yes This is leap year. ");
    else
    printf("Sorry! This is not leap year. ");

    return 0;
}
 ```
 ## 12. wap to merge two sorted array such that the resultant array is also sorted
 ## c++
 ```c++
 // Online C++ compiler to run C++ program online
#include <iostream>

using namespace std;

int mergeSort (int a1[], int a2[], int a3[], int n, int m){
    
    int i,j,k;
    i = j = k = 0;
    
    for(i = 0; i < n && j < m; ){
        
         if(a1[i] < a2[j]){
            
            a3[k] = a1[i];
            i++;
            k++;
        }
        else {
            a3[k] = a2[j];
            k++;
            j++;
        }
    }
    while(i < n){
        a3[k] = a1[i];
        i++;
        k++;
    }
    while(j < m){
        a3[k] = a2[j];
        j++;
        k++;
    }
}

int main() {
    // Write C++ code here
    int n, m;
    cout << "Enter the size of the Array 1 :  ";
    cin>> n;
    cout << "\nEnter the size of the Array 2 :  ";
    cin>> m;
    
    int *arr1 = NULL;
    arr1 = (int*)malloc(n*(sizeof(int)));
    int *arr2 = NULL;
    arr2 = (int*)malloc(m*(sizeof(int)));
    int *arr3 = NULL;
    arr3 = (int*)malloc((n+m)*(sizeof(int)));
    
    int i;
    cout<<"\nEnter the Array1 Element : ";
    for(i = 0; i < n; i++){
        cin>>arr1[i];
    }
    cout<<"\nEnter the Array2 Element : ";
    for(i = 0; i < n; i++){
        cin>>arr2[i];
    }
    
    mergeSort(arr1, arr2, arr3, n, m);
    cout<<"Array after merge Sort:  ";
    for(i = 0; i < n+m; i++){
        cout<<arr3[i]<<" ";
    }
    cout<<"\n";

    return 0;
}
 ```

 ## 13.wap to find GCD(HCF) of two number
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int num1, num2,gcd = 0;
    printf("Enter first number : ");
    scanf("%d",&num1);
    printf("Enter second number : ");
    scanf("%d",&num2);
    
    if(num1 > num2){
        int temp = num1;
        num1 = num2;
        num2 = temp;
    }
    
    for(int i = 1; i < num1; i++){
        
        if((num1 % i == 0) && (num2 % i == 0)){
            gcd = i;
        }
    }
    if(gcd)
    printf("GCD is : %d",gcd);
    else
    printf("GCD is : 1");

    return 0;
}
 ```

 ## 14.wap to add two fraction number and display their sum in reduced form
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int n1,d1,n2,d2;
    printf("Enter first number like n/d : ");
    scanf("%d %d",&n1, &d1);
    printf("Enter second number like n/d : ");
    scanf("%d %d",&n2, &d2);
    
    int resN = (n1 * d2) + (n2 * d1);
    int resD = (d1 * d2);
    int temp;
    if(resN >= resD)
    temp = resD;
    else
    temp = resN;
    for(int i = temp; i > 0; i--){
        
        if((resD % i == 0) && (resN % i == 0))
        {
           resD = resD / i;
           resN = resN / i;
           break;
        }
    }
    
    printf("Result is : %d  %d", resN,resD);

    return 0;
}
 ```

 ## 15.wap to find the number of integer with exactly 9 divisor.
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int num, dup,  count = 0,arr[10];
    printf("Enter the number: ");
    scanf("%d", &num);
    
    for(int i = num; i > 0; i--){
        
        dup = i;
        int iteration = 0;
        for(int j = 1; j <= dup; j++){
            
            if(dup % j == 0)
            iteration++;
        
        }
        if(iteration == 9){
            
            arr[count] = dup;
            count++;
        }
    }
    if(count){
        printf("%d", count);
        for(int i = 0; i < count; i++){
            printf(" %d", arr[i]);
        }
    }

    return 0;
}
 ```

 ## 16. Given two positive integer N and X, where N is the number of total patients and X is the time duration (in minute) after which a new patient arrives. Also a doctor will give only 10 minute to each patient. The task is to calculate the time (in minute) to Last patient needs to wait.
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int n, x;
    printf("Enter the number of patient: ");
    scanf("%d", &n);
    printf("Enter the arrival time : ");
    scanf("%d", &x);
    
    int wait = (((n - 1) * 10) -(n - 1) * x);
   printf("Waiting for...: %d", wait);

    return 0;
}
 ```
 ## 17.wap to reverse the string
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <string.h>

int main() {
    // Write C code here
    char st[10000];
    printf("Enter String : ");
    scanf("%s", &st);
   int i = 0;
   int j = strlen(st) - 1;
   while(i < j){
       char a = st[i];
       st[i] = st[j];
       st[j] = a;
       i++;
       j--;
   }
  printf("%s", st);


    return 0;
}
 ```

 ## 21. User wrote a sequence of words,The words are written using the rules given below. The sequence is concatenation ofone or more   words consisting of english latter. All the latter of first word is lowercase. For each of the sub sequent words, the first latter is uppercase and rest is lowercase.You need to find out the words in the string.
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <string.h>

int main() {
    // Write C code here
    char st[10000];
    int i , cnt = 0;
    scanf("%s", &st);
    for(i = 0; i < strlen(st); i++){
        if(st[i] >= 65 && st[i] <= 90){
            cnt++;
        }
    }
    printf("%d", cnt+1);

    return 0;
}
 ``` 

 ## 22.You are a traveller, lost in a jungle. But you have the Map with you . And you remember the route you travelled so you will backtrack and reach the Starting point. Your task is to print the starting point.
 ## Input: First line consists of T test cases.Each test cases consits of 3 lines. First line of each test case consist of two integer X, Y denoting of your current location. Second line each test case consist of an integer N denoting of number of paths you travelled. Third line of each test case consist of 2*N spaced integer Xi, Yj denoting the pionts at the paths you travelled.

 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>

int main() {
    // Write C code here
    int cx, cy, x, y, n;
    scanf("%d %d", &cx, &cy);
    scanf("%d", &n);
    while(n--){
        scanf("%d %d", &x, &y);
        cx -= x;
        cy -= y;
    }
    printf("%d %d ", cx, cy);

    return 0;
}
 ```

 ## 23. Given an array of integer, the task is to find whether it's possible to construct an integer using all the digits of these numbers such that it would be divided by 3. If it possible then print "1" and if not print "0";
 ## c
 ```c
 // Online C compiler to run C program online
#include <stdio.h>
#include <stdlib.h>

int main() {
    // Write C code here
    int n;
    printf("Enter the length of Array : ");
    scanf("%d", &n);
    int *ptr = NULL;
    ptr = (int*)malloc(n*sizeof(int));
    printf("Enter the array element : ");
    for(int i = 0; i < n; i++){
        scanf("%d", ptr+1);
    }
    
    int i, sum = 0,flag = 1;
    for( i = 1; i < n; i++){
        
        if(ptr[i] % 3 == 0){
            printf("Yes divisible by 3, So 1 ");
            i = n;
            flag = 0;
            break;
        }
        else {
        while(ptr[i]){
            
            sum = sum + (ptr[i] % 10);
            ptr[i] = ptr[i] / 10;
        }
    }
    }
    if(sum % 3 == 0 && sum)
        printf("Yes divisible by 3, So 1");
    else if(i  != n || flag)
    printf("No!, So  0");
    
    return 0;
}
 ```