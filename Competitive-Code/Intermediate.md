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