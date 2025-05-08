# EX 42 C program to write a fuctions to perform push,pop,display,peek in stack using array.
## DATE:08/05/2025
## AIM: To write a fuctions to perform push,pop,display,peek in stack using array.

## Algorithm
1. Start. 
2. Define a variables. 
3. Write a functions to perform push,pop,display,peek in stack using array. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End.  

## Program:
```
int stack[100]; 
int size=3,top=-1,i; 
void push (float data) 
{ 
if(top==size-1) 
{ 
printf("stack is full\n"); 
} 
else{ 
top=top+1; 
stack[top]=data;} 
} void display(){ 
for(i=top; i>=0; i--){ 
printf("%d ",stack[i]); 
} 
if(top==-1) 
{ 
printf("stack is empty\n"); 
} 
Void pop() 
{ 
if(top==-1) 
{ 
printf("stack is empty\n"); 
} 
else{ 
top=top-1; 
} 
} 
void peek() 
{ 
printf("%d ",stack[top]); 
} 
/*
C program to write a fuctions to perform push,pop,display,peek in stack using array.
Developed by: 
RegisterNumber:  
*/
```

## Output:

push(10);

push(20);

push(30);

display();

peek();

push(40);

pop();

display();

pop();

pop();

display();


30   20   10   30   stack is full

20   10  stack is empty


## Result:
Thus the program was executed and the output was verified successfully.
