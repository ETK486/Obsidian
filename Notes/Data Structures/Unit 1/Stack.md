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

###### [[Implementation of Stack using Array]]

###### [[Implementation of Stack using Linked List]]

