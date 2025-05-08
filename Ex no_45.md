# EX 45 C program that implements a queue using an array, and performs insertion (enqueue) and display operations.
## DATE:08/05/2025
## AIM: To write a C program that implements a queue using an array, and performs insertion (enqueue) and display operations. 

## Algorithm
1. Start
2. Initialize the queue with front = -1 and rear = -1.
3. On enqueue, check for overflow. If not full, insert at rear + 1 and adjust front if needed.
4. On display, print elements from front to rear if queue is not empty. 
5.  End. 

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
    if (front == -1)
        front = 0;
    rear++;
    queue[rear] = value;
    printf("Inserted %d\n", value);
}

// Function to display queue elements
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
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();  // Show inserted items

    return 0;
}

/*
C program that implements a queue using an array, and performs insertion (enqueue) and display operations.
Developed by: 
RegisterNumber:  
*/
```

## Output:
Inserted 10
Inserted 20
Inserted 30
Queue elements: 10 20 30


## Result:
Thus the program was executed and the output was verified successfully.
