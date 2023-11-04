	A stack is a linear data structure in which the insertion of a new element and removal of an existing element takes place at the same end represented as the top of the stack. To implement the stack, it is required to maintain the pointer to the top of the stack, which is the last element to be inserted because we can access the elements only on the top of the stack.

##### Basic Operations on Stack

In order to make manipulations in a stack, there are certain operations provided to us.

- **push()** to insert an element into the stack
- **pop()** to remove an element from the stack
- **top()** Returns the top element of the stack.
- **isEmpty()** returns true if stack is empty else false.
- **size()** returns the size of stack.

![[Pasted image 20231104221817.png]]

## **Push:**

	Adds an item to the stack. If the stack is full, then it is said to be an Overflow condition.

**Algorithm for push:**

	begin
	 if stack is full
	    return
	 endif
	 else  
		 increment top
		 stack[top] assign value
	 end else
	 end procedure

## **Pop:**

	Removes an item from the stack. The items are popped in the reversed order in which they are pushed. If the stack is empty, then it is said to be an Underflow condition.

**Algorithm for pop:**

	begin
		 if stack is empty
		    return
		 endif
		 else
			 store value of stack[top]
			 decrement top
			 return value
		 end else
	end procedure

## **Top:**

	Returns the top element of the stack.

**Algorithm for Top:**

	begin 
	  return stack[top]
	end procedure

## **isEmpty:**

	Returns true if the stack is empty, else false.

**Algorithm for isEmpty**:

	begin
		 if top < 1
		    return true
		else
		    return false
	 end procedure

### Implementing Stack using Arrays:

	/* C++ program to implement basic stack 
	operations */
	#include <bits/stdc++.h> 
	using namespace std; 
	#define MAX 1000 
	class Stack { 
		int top; 
	public: 
		int a[MAX]; // Maximum size of Stack 
		Stack() { top = -1; } 
		bool push(int x); 
		int pop(); 
		int peek(); 
		bool isEmpty(); 
	}; 
	bool Stack::push(int x) 
	{ 
		if (top >= (MAX - 1)) { 
			cout << "Stack Overflow"; 
			return false; 
		} 
		else { 
			a[++top] = x; 
			cout << x << " pushed into stack\n"; 
			return true; 
		} 
	} 
	int Stack::pop() 
	{ 
		if (top < 0) { 
			cout << "Stack Underflow"; 
			return 0; 
		} 
		else { 
			int x = a[top--]; 
			return x; 
		} 
	} 
	int Stack::peek() 
	{ 
		if (top < 0) { 
			cout << "Stack is Empty"; 
			return 0; 
		} 
		else { 
			int x = a[top]; 
			return x; 
		} 
	} 
	bool Stack::isEmpty() 
	{ 
		return (top < 0); 
	} 
	// Driver program to test above functions 
	int main() 
	{ 
		class Stack s; 
		s.push(10); 
		s.push(20); 
		s.push(30); 
		cout << s.pop() << " Popped from stack\n"; 	
		//print top element of stack after popping 
		cout << "Top element is : " << s.peek() << endl; 	
		//print all elements in stack : 
		cout <<"Elements present in stack : "; 
		while(!s.isEmpty()) 
		{ 
			// print top element in stack 
			cout << s.peek() <<" "; 
			// remove top element in stack 
			s.pop(); 
		} 
		return 0; 
	}

### Implementing Stack using Linked List:

	 // C++ program for linked list implementation of stack 
	#include <bits/stdc++.h> 
	using namespace std; 
	// A structure to represent a stack 
	class StackNode { 
	public: 
		int data; 
		StackNode* next; 
	}; 
	StackNode* newNode(int data) 
	{ 
		StackNode* stackNode = new StackNode(); 
		stackNode->data = data; 
		stackNode->next = NULL; 
		return stackNode; 
	} 
	int isEmpty(StackNode* root) 
	{ 
		return !root; 
	} 
	void push(StackNode** root, int data) 
	{ 
		StackNode* stackNode = newNode(data); 
		stackNode->next = *root; 
		*root = stackNode; 
		cout << data << " pushed to stack\n"; 
	} 
	int pop(StackNode** root) 
	{ 
		if (isEmpty(*root)) 
			return INT_MIN; 
		StackNode* temp = *root; 
		*root = (*root)->next; 
		int popped = temp->data; 
		free(temp); 
		return popped; 
	} 
	int peek(StackNode* root) 
	{ 
		if (isEmpty(root)) 
			return INT_MIN; 
		return root->data; 
	} 
	// Driver code 
	int main() 
	{ 
		StackNode* root = NULL; 
		push(&root, 10); 
		push(&root, 20); 
		push(&root, 30); 
		cout << pop(&root) << " popped from stack\n"; 
		cout << "Top element is " << peek(root) << endl; 
		cout <<"Elements present in stack : "; 
		//print all elements in stack : 
		while(!isEmpty(root)) 
		{ 
			// print top element in stack 
			cout << peek(root) <<" "; 
			// remove top element in stack 
			pop(&root); 
		} 
		return 0; 
	} 
