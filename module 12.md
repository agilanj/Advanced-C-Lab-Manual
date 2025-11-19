

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

```
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{
    struct Node *temp = malloc (sizeof(struct Node));
    temp = head;
    while(temp != NULL){
        printf("%c\n", temp->data);
        temp = temp->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/56fd345f-a3e4-41b1-aac1-2579df1c9258)


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C FUNCTION TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

Aim:
To write a C function to pop an element from the given stack using liked list.

Algorithm:
1. Check if head is NULL:
    a. If yes, print "stack is empty" and return.
2. Else:
    a. Set a temporary pointer temp to head.
    b. Update head to point to the next node (head = head->next).
    c. Free the memory allocated to temp to remove the popped node.
 
Program:

```
struct Node   
{  
char data[20];  
struct Node *next;  
}*head;  
void pop()  
{
    struct Node *temp = malloc(sizeof(struct Node));
    if(head == NULL){
        printf("stack is empty\n");
    }
    else{
        temp = head;
        head = temp->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/513070ef-4517-4965-8e20-71fce0568bba)


Result:
Thus, the function to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C FUNCTION TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:
To write a C function to display queue elements using linked list.

Algorithm:
1. Set a temporary pointer temp to front.
2. If temp is NULL:
    a. Print "queue is empty".
3. Else:
    a. Print "queue elements:".
    b. While temp is not NULL:
        i. Print the character data at temp.
        ii. Move temp to temp->next.
 
Program:

```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp = front;
    if(temp == NULL){
        printf("queue is empty\n");
    }
    else{
        printf("queue elements:\n");
        while(temp != NULL){
            printf("%c\n", temp->data);
            temp = temp->next;
        }
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/ff6fdacb-8e03-4e69-905c-6707fb459975)


Result:
Thus, the function to display queue elements using linked list is verified successfully.


 
EXP NO:29 C FUNCTION TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C function to insert elements in queue using linked list

Algorithm:
1. Allocate a new node n and assign data to n->data.
2. Set n->next to NULL (because it will be the last node).
3. If the queue is empty (front == NULL):
   a. Set both front and rear to n.
4. Else:
   a. Link the current rear node's next pointer to n.
   b. Update rear to point to n.

 
Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node *n = malloc (sizeof(struct Node));
    n->data = data;
    n->next = NULL;
    if(front == NULL){
        front = rear = n;
    }
    else{
        rear->next = n;
        rear = n;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/877a9350-4035-45fa-b9a8-a626e8a7621c)


Result:
Thus, the function to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1. Check if front is NULL:
   a. If yes, print "Queue is empty" and return.
2. Otherwise, print the data stored at front node.

Program:

```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%c\n", front->data);
}
```

Output:

![image](https://github.com/user-attachments/assets/956f90ac-7122-49ed-8b45-2e79bd15313d)


Result:

Thus, the function to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


