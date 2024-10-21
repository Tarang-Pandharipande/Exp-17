# Experiment 17



## Aim:
To study and implement Linked List


## Apparatus:
Vs Code, Github


## Theory:

A linked list is a data structure used in C++ and other programming languages to store a collection of elements, where each element or node contains both data and a reference to the next node in the sequence. Unlike arrays, linked lists are dynamic in nature, allowing for insertion and deletion of elements at any position without needing to shift other elements.

### Node:
The fundamental building block of a linked list. Each node contains two parts:
1: Data: The value or information stored in the node.
2: Pointer: A reference to the next node in the list.

### Head:
The first node in the linked list. The head points to the first node, which then points to the second node, and so on.

### Tail:
The last node in the linked list. The tail's next pointer is nullptr (or NULL), indicating the end of the list.

## Types of linked lists:

### Singly linked:
Each node contains data and a pointer to the next node. It allows traversal in one direction (forward).

### Doubly linked:
Each node contains data, a pointer to the next node, and a pointer to the previous node. It supports bidirectional traversal.

### Circular linked list:
The last node points back to the first node, forming a circular structure. It can be singly or doubly linked.

## Code:

### Singly linked: 
```
#include<iostream>
using namespace std;

class Link {
    public:
    int data;
    Link* next;

    Link(int num){
        data=num;
        next=NULL;
    } 
};

int main(){
    Link* l1 = new Link(6);
    cout<<l1->data<<"   "<<l1->next;
}
```
### Output:
![image_2024-10-21_140903352](https://github.com/user-attachments/assets/219e9a33-aee8-4bdf-b3d5-d54b6ca5ca96)


### Doubly linked list:
```
#include<iostream>
using namespace std;

class Link {
    public:
    int data;
    Link* next;

    Link(int num){
        data=num;
        next=NULL;
    }
};
void insert_head(Link* &head, int data){
    Link* new_node=new Link(data);
    new_node->next = head;
    head = new_node;
}
void disp(Link* head){
    Link* temp = head;
    while(temp!=NULL){
        cout<<temp->data<<"->";
        temp = temp->next;
    }
    cout<<"NULL"<<endl;
}

int main(){
    Link* head = NULL;
    insert_head(head, 30);
    disp(head);
    insert_head(head, 32);
    disp(head);
    insert_head(head, 35);
    disp(head);
}
```
### Output:
![image_2024-10-21_141434480](https://github.com/user-attachments/assets/0aa84970-b57e-4eaa-a7b4-5a95e743f7e5)


## Conclusion:
This program helps us understand the syntax of linked lists in C++ and different types of linked lists such as singly linked, doubly linked and circular linked.
