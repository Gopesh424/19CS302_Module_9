# EX 43 C program to Write a function to display queue elements using array.
## DATE:08/05/2025
## AIM: To Write a function to display queue elements using array.

## Algorithm
1. Start. 
2. Define a variables. 
3. Write a function to display queue elements using array. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End.  

## Program:
```
#include <stdio.h>
#define SIZE 100

int queue[SIZE];
int front = -1, rear = -1;

// Function to add element to the queue
void enqueue(int value) {
    if (rear == SIZE - 1) {
        printf("Queue is full (Overflow)\n");
        return;
    }
    if (front == -1) front = 0;  // First element
    rear++;
    queue[rear] = value;
    printf("Inserted %d\n", value);
}

// Function to remove element from the queue
void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue is empty (Underflow)\n");
        return;
    }
    printf("Deleted %d\n", queue[front]);
    front++;
}

// Function to display elements of the queue
void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty\n");
        return;
    }

    printf("Queue elements: ");
    for (int i = front; i <= rear; i++) {
        printf("%d ", queue[i]);
    }
    printf("\n");
}

int main() {
    // Sample usage
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    dequeue();
    display();

    return 0;
}

/*
C program to write a function to display queue elements using array.
Developed by: 
RegisterNumber:  
*/
```

## Output:
Inserted 10
Inserted 20
Inserted 30
Queue elements: 10 20 30
Deleted 10
Queue elements: 20 30


## Result:
Thus the program was executed and the output was verified successfully.
