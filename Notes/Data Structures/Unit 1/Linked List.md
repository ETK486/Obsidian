	A Linked List is a linear data structure which looks like a chain of nodes, where each node is a different element. Unlike Arrays, Linked List elements are not stored at a contiguous location. It is basically chains of nodes, each node contains information such as data and a pointer to the next node in the chain. In the linked list there is a head pointer, which points to the first element of the linked list, and if the list is empty then it simply points to null or nothing.

###### Advantages:

Here are a few advantages of a linked list that is listed below, 
- Dynamic Data structure: The size of memory can be allocated or de-allocated at run time based on the operation insertion or deletion.
- Ease of Insertion/Deletion: The insertion and deletion of elements are simpler than arrays since no elements need to be shifted after insertion and deletion, Just the address needed to be updated.
- Efficient Memory Utilization: As we know Linked List is a dynamic data structure the size increases or decreases as per the requirement so this avoids the wastage of memory. 
- Implementation: Various advanced data structures can be implemented using a linked list like a stack, queue, graph, hash maps, etc.

###### Types of linked lists:

There are mainly three types of linked lists:

1. Single-linked list
2. Double linked list
3. Circular linked list

#### Singly-linked list:

	Traversal of items can be done in the forward direction only due to the linking of every node to its next node.
![[Pasted image 20231104213526.png]]
###### Declaration in C++:

	// A Single linked list node
	class Node { 
	public:
		int data;
		Node* next;
	}; 

###### Operations on Singly Linked List:

The following operations are performed on a Single Linked List

- Insertion: The insertion operation can be performed in three ways. They are as follows…
    - Inserting At the Beginning of the list
    - Inserting At End of the list
    - Inserting At Specific location in the list
- Deletion: The deletion operation can be performed in three ways. They are as follows…
    - Deleting from the Beginning of the list
    - Deleting from the End of the list
    - Deleting a Specific Node
- Search: It is a process of determining and retrieving a specific node either from the front, the end or anywhere in the list.
- Display: This process displays the elements of a Single-linked list.

#### Doubly Linked List:

Traversal of items can be done in both forward and backward directions as every node contains an additional previous pointer that points to the previous node.

![[Pasted image 20231104214510.png]]

###### Declaration in C++:
	/* Node of a doubly linked list */
	class Node {
	public:
		int data;
		Node* next; // Pointer to next node in DLL
		Node* prev; // Pointer to previous node in DLL
	};

###### Operations on Double-Linked List:

In a double-linked list, we perform the following operations…

- Insertion: The insertion operation can be performed in three ways as follows:
    - Inserting At the Beginning of the list
    - Inserting after a given node.
    - Inserting at the end
    - Inserting before a given node
- Deletion: The deletion operation can be performed in three ways as follows…
    - Deleting from the Beginning of the list
    - Deleting from the End of the list
    - Deleting a Specific Node
- Display: This process displays the elements of a double-linked list.

#### Circularly Linked List:
	A circular linked list is a type of linked list in which the first and the last nodes are also connected to each other to form a circle, there is no NULL at the end.

![[Pasted image 20231104214953.png]]

###### operations on Circular Linked List:

The following operations are performed on a Circular Linked List

- Insertion: The insertion operation can be performed in three ways:
    - Insertion in an empty list
    - Insertion at the beginning of the list
    - Insertion at the end of the list
    - Insertion in between the nodes
- Deletion: The deletion operation can be performed in three ways:
    - Deleting from the Beginning of the list
    - Deleting from the End of the list
    - Deleting a Specific Node
- Display: This process displays the elements of a Circular linked list.