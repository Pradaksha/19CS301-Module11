# Exp.No: 11(e) DOUBLY LINKED LIST 
## DOUBLY LINKED LIST 
## Note: Write a python program to print the elements in forward and reverse direction in doubly linked list. 

### AIM  
To Write a python program to print the elements in forward and reverse direction in doubly linked list. 


### ALGORITHM

Create Node class with data, next, and prev.

Create DoublyLinkedList class with head = None.

push(data):

Insert at the beginning.

Update head and previous links.

append(data):

Insert at the end.

Traverse to the last node and update links.

printList(node):

Traverse forward using next and print data.

Then traverse backward using prev and print data.

Insert nodes using push and append.

Print list in both directions.

### PROGRAM
```
## Reg no:212223020020
## Name:Pradaksha V

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
  
class DoublyLinkedList:
    def __init__(self):
        self.head = None
  
    def push(self, new_data):
        new_node = Node(new_data)
        new_node.next = self.head
        if self.head is not None:
            self.head.prev = new_node
        self.head = new_node
        
    def append(self, new_data):
        new_node = Node(new_data)
        if self.head is None:
           self.head = new_node
           return
        last = self.head
        while last.next:
            last = last.next
        last.next = new_node
        new_node.prev = last
        return
  
    def printList(self, node):
        print("\nTraversal in forward direction")
        while node:
          
            print(node.data)
            last = node
            node = node.next
        print("\nTraversal in reverse direction")
        while last:
           
            print(last.data)
            last = last.prev
  
llist = DoublyLinkedList()
  
llist.append(6)
llist.push(7)
llist.push(1)
llist.append(4)
print ("Created DLL is: ")
llist.printList(llist.head)
  
```

### OUTPUT  
![image](https://github.com/user-attachments/assets/bd38eba2-6532-4bc5-9447-e2056e51cc3b)


### RESULT
The created doubly linked list contains the elements in forward direction as: 1, 7, 6, 4. When traversed in reverse direction, the elements are: 4, 6, 7, 1.
