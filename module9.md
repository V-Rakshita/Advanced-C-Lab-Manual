# EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim:
To write a C program to display stack elements using an array.
## Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
## Program:

```c
#include <stdio.h>

int main() {
    int stack[5];
    int top = -1;

    
    top++; stack[top] = 10;
    top++; stack[top] = 20;
    top++; stack[top] = 30;

    
    if (top == -1) {
        printf("Stack is empty\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d ", stack[i]);
        }
        printf("\n");
    }

    return 0;
}
```

## Output:

<img width="289" height="143" alt="image" src="https://github.com/user-attachments/assets/884e65a5-9705-4927-b70d-21f9d545fc0d" />




## Result:
Thus, the program to display stack elements using an array is verified successfully.
 

# EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
## Aim:
To create a C program to push the given element in to a stack using array.
## Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
## Program:

```c
#include <stdio.h>

void push(float stack[], int *top, int size, float element) {
    if (*top == size - 1) {
        printf("Stack Overflow\n");
    } else {
        (*top)++;
        stack[*top] = element;
        printf("%.2f pushed into stack\n", element);
    }
}

int main() {
    float stack[5];
    int top = -1;
    int size = 5;

    push(stack, &top, size, 10.5f);
    push(stack, &top, size, 20.8f);
    push(stack, &top, size, 30.2f);

    return 0;
}
```

## Output:

<img width="328" height="156" alt="image" src="https://github.com/user-attachments/assets/2a2dbddb-8a2a-4f11-abc9-dd7a9c953127" />





## Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
# EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
## Aim:
To write a C program to display queue elements using array

## Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
## Program:

```c
#include <stdio.h>

int main() {
    int queue[5];
    int front = -1, rear = -1;

   
    rear++; queue[rear] = 10; if (front == -1) front = 0;
    rear++; queue[rear] = 20;
    rear++; queue[rear] = 30;

    
    if (front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("Queue elements are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }

    return 0;
}
```

## Output:

<img width="270" height="126" alt="image" src="https://github.com/user-attachments/assets/de85942d-df9d-4d3a-a869-daab10b2e53a" />



## Result:
Thus, the program to display queue elements using array is verified successfully.


 
# EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
## Aim:
To write a C program to insert elements in queue using array.

## Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

## Program:

```c
#include <stdio.h>

void enqueue(float queue[], int *front, int *rear, int size, float value) {
    if (*rear == size - 1) {
        printf("Queue Overflow\n");
    } else {
        if (*front == -1) *front = 0;
        (*rear)++;
        queue[*rear] = value;
        printf("%.2f inserted into queue\n", value);
    }
}

int main() {
    float queue[5];
    int front = -1, rear = -1;
    int size = 5;

    enqueue(queue, &front, &rear, size, 12.5f);
    enqueue(queue, &front, &rear, size, 45.7f);
    enqueue(queue, &front, &rear, size, 33.3f);

    return 0;
}
```

## Output:

<img width="332" height="149" alt="image" src="https://github.com/user-attachments/assets/72ba7eb2-14b5-4bd3-af43-e173f797e762" />


## Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
# EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



## Aim:

To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



## Program:

```c
#include <stdio.h>

void dequeue(int queue[], int *front, int *rear) {
    if (*front == -1) {
        printf("Queue is empty\n");
    } else {
        printf("Deleted element: %d\n", queue[*front]);
        (*front)++;
        if (*front > *rear) {
            *front = *rear = -1;
        }
    }
}

int main() {
    int queue[5];
    int front = -1, rear = -1;

    // sample insertions
    rear++; queue[rear] = 10; if (front == -1) front = 0;
    rear++; queue[rear] = 20;
    rear++; queue[rear] = 30;

    dequeue(queue, &front, &rear);
    dequeue(queue, &front, &rear);
    dequeue(queue, &front, &rear);
    dequeue(queue, &front, &rear); // show empty

    return 0;
}
```

## Output:

<img width="265" height="186" alt="image" src="https://github.com/user-attachments/assets/b72e218d-366d-45dd-805d-075f4d2ff273" />



## Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
