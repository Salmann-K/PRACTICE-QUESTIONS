
## OUTPUT BASED

1-What is the output of following program?

include <stdio.h>

void fun(int x)

{
   
   x = 30;
   
}

int main()
{
  
  int y = 20;

  fun(y);

  printf("%d", y);

  return 0;

}

A) 30    B)20    C)Compiler Error    D)Runtime Error

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-1/)


Question 2

Output of following program?

include <stdio.h>

void fun(int *ptr)
{
    
    *ptr = 30;
    
}
 
int main()
{
  
  int y = 20;
 
  fun(&y);

  printf("%d", y);
 
  return 0;

}

A) 20    B)30    C)Compiler Error    D)Runtime Error

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-2/)


Question 3

Output of following program?

include <stdio.h>
 
int main()
{
    
    int *ptr;
    
    int x;
 
    ptr = &x;
    
    *ptr = 0;
 
    printf(" x = %dn", x);
    
    printf(" *ptr = %dn", *ptr);
 
    *ptr += 5;
    
    printf(" x  = %dn", x);
    
    printf(" *ptr = %dn", *ptr);
 
    (*ptr)++;
    
    printf(" x = %dn", x);
    
    printf(" *ptr = %dn", *ptr);
 
    return 0;

}

A) x = 0,*ptr = 0,x = 5,*ptr = 5,x = 6,*ptr = 6

B) x = garbage value,*ptr = 0,x = garbage value,*ptr = 5,x = garbage value,*ptr = 6

C) x = 0,*ptr = 0,x = 5,*ptr = 5,x = garbage value,*ptr = garbage value

D) x = 0,*ptr = 0,x = 0,*ptr = 0,x = 0,*ptr = 0

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-3/)


Consider a compiler where int takes 4 bytes, char takes 1 byte and pointer takes 4 bytes.

include <stdio.h>
 
int main()
{
 
    int arri[] = {1, 2 ,3};
    
    int *ptri = arri;
 
    char arrc[] = {1, 2 ,3};
    
    char *ptrc = arrc;
 
    printf("sizeof arri[] = %d ", sizeof(arri));
    
    printf("sizeof ptri = %d ", sizeof(ptri));
 
    printf("sizeof arrc[] = %d ", sizeof(arrc));
    
    printf("sizeof ptrc = %d ", sizeof(ptrc));
 
    return 0;

}

A) sizeof arri[] = 3 sizeof ptri = 4 sizeof arrc[] = 3 sizeof ptrc = 4

B)sizeof arri[] = 12 sizeof ptri = 4 sizeof arrc[] = 3 sizeof ptrc = 1

C)sizeof arri[] = 3 sizeof ptri = 4 sizeof arrc[] = 3 sizeof ptrc = 1

D)sizeof arri[] = 12 sizeof ptri = 4 sizeof arrc[] = 3 sizeof ptrc = 4

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-4/)


Question 5

Assume that float takes 4 bytes, predict the output of following program.

include <stdio.h>
 
int main()
{

    float arr[5] = {12.5, 10.0, 13.5, 90.5, 0.5};
    
    float *ptr1 = &arr[0];
    
    float *ptr2 = ptr1 + 3;
 
    printf("%f ", *ptr2);
    
    printf("%d", ptr2 - ptr1);
 
    return 0;

}

A)90.500000 3   B)90.500000 12   C)10.000000 12   D)0.500000 3

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-5/)


Question 6

include<stdio.h>

int main()
{

    int arr[] = {10, 20, 30, 40, 50, 60};
    
    int *ptr1 = arr;
    
    int *ptr2 = arr + 5;
    
    printf("Number of elements between two pointer are: %d.", 
                                (ptr2 - ptr1));
    
    printf("Number of bytes between two pointers are: %d",  
                              (char*)ptr2 - (char*) ptr1);
    return 0;

}

A) Number of elements between two pointer are: 5. Number of bytes between two pointers are: 20
B) Number of elements between two pointer are: 20. Number of bytes between two pointers are: 20
C) Number of elements between two pointer are: 5. Number of bytes between two pointers are: 5
D) Compiler Error
E) Runtime Error

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-6/) 


Question 7

include<stdio.h> 

int main() 
{

   int a; 
   
   char *x; 
   
   x = (char *) &a; 
   
   a = 512; 
   
   x[0] = 1; 
   
   x[1] = 2; 
   
   printf("%dn",a);   
   
   return 0; 

}

A) Machine dependent  B) 513  C) 258  D) Compiler Error

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-7/)


Question 8

int main()
{

 char *ptr = "GeeksQuiz";
 
 printf("%cn", *&*&*ptr);
 
 return 0;

}

A) Compiler Error    B) Garbage Value    C) Runtime Error    D) G

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-8/)


Question 9

include<stdio.h>

void fun(int arr[])
{

  int i;
  
  int arr_size = sizeof(arr)/sizeof(arr[0]);
  
  for (i = 0; i < arr_size; i++)
      
      printf("%d ", arr[i]);

}
 
int main()
{

  int i;
  
  int arr[4] = {10, 20 ,30, 40};
  
  fun(arr);
  
  return 0;

} 

A) 10 20 30 40     B) Machine Dependent     C) 10 20      D) Northing

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-11-2/)


Question 10

The reason for using pointers in a C program is

A) Pointers allow different functions to share and modify their local variables.

B) To pass large structures so that complete copy of the structure can be avoided.

C) Pointers enable complex “linked" data structures like linked lists and binary trees.

D) All of the above

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-12/)


Question 11

include<stdio.h> 

void f(int *p, int *q) 
{ 
  
  p = q; 
  
  *p = 2; 

} 

int i = 0, j = 1; 

int main() 
{ 
  
  f(&i, &j); 
  
  printf("%d %d n", i, j); 
  
  getchar(); 
  
  return 0; 

}

A) 2 2      B) 2 1      C) 0 1      D) 0 2

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-13/)


Question 12

Consider this C code to swap two integers and these five statements after it:

void swap(int *px, int *py) 
{ 

   *px = *px - *py; 
   
   *py = *px + *py; 
   
   *px = *py - *px; 

}

S1: will generate a compilation error S2: may generate a segmentation fault at runtime depending on the arguments passed S3: correctly implements the swap procedure for all input pointers referring to integers stored in memory locations accessible to the process S4: implements the swap procedure correctly for some but not all valid input pointers S5: may add or subtract 
integers and pointers.

A) S1

B) S2 and S3

C) S2 and S4

D) S2 and S5

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-14/)


Question 13

int f(int x, int *py, int **ppz) 
{

  int y, z; 
  
  **ppz += 1; 
  
  z  = **ppz; 
  
  *py += 2; 
  
  y = *py; 
  
  x += 3; 
  
  return x + y + z; 

} 
   
void main() 
{

   int c, *b, **a; 
   
   c = 4; 
   
   b = &c; 
   
   a = &b; 
   
   printf("%d ", f(c, b, a)); 
   
   return 0;

}

A) 18     B) 19     C) 21     D) 22

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-15/)


Question 14

Predict the output of following program

include<stdio.h>

int main()
{

    int a = 12;
    
    void *ptr = (int *)&a;
    
    printf("%d", *ptr);
    
    getchar();
    
    return 0;

}

A) 12     B) Compiler Error     C) RunTime Error     D) 0

[ANSWER](https://www.geeksforgeeks.org/c-pointers-question-16/)


Question 15

include<stdio.h>
 
void swap (char *x, char *y)
{

    char *t = x;
    
    x = y;
    
    y = t;

}

int main()
{

    char *x = "geeksquiz";
    
    char *y = "geeksforgeeks";
    
    char *t;
    
    swap(x, y);
    
    printf("(%s, %s)", x, y);
    
    t = x;
    
    x = y;
    
    y = t;
    
    printf("n(%s, %s)", x, y);
    
    return 0;

}

A)(geeksquiz, geeksforgeeks) (geeksforgeeks, geeksquiz)

B)(geeksforgeeks, geeksquiz) (geeksquiz, geeksforgeeks)

C)(geeksquiz, geeksforgeeks) (geeksquiz, geeksforgeeks)

D(geeksforgeeks, geeksquiz) (geeksforgeeks, geeksquiz)

[ANSWER](https://www.geeksforgeeks.org/c-pointer-basics-question-15/)
