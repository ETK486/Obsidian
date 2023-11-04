	A Queue is defined as a linear data structure that is open at both ends and the operations are performed in First In First Out (FIFO) order. We define a queue to be a list in which all additions to the list are made at one end, and all deletions from the list are made at the other end.  The element which is first pushed into the order, the operation is first performed on that.

![[Pasted image 20231104230204.png]]

#### **Characteristics of Queue:**

- Queue can handle multiple data.
- We can access both ends.
- They are fast and flexible. 

#### Queue Representation:

###### Array Representation of Queue:

	// Creating an empty queue
	// A structure to represent a queue
	class Queue {
	public:
		int front, rear, size;
		unsigned cap;
		int* arr;
	};
	// Function to create a queue of given capacity
	// It initializes size of queue as 0
	Queue* createQueue(unsigned cap)
	{
		Queue* queue = new Queue();
		queue->cap = cap;
		queue->front = queue->size = 0;
		queue->rear = cap - 1;
		queue->arr = new int[(queue->cap * sizeof(int))];
		return queue;
	}

###### Linked List Representation of Queue:

	struct QNode {
		int data;
		QNode* next;
		QNode(int d)
		{
			data = d;
			next = NULL;
		}
	};
	struct Queue {
		QNode *front, *rear;
		Queue() { front = rear = NULL; }
	};

#### Basic Operations for Queue in Data Structure:

Some of the basic operations for Queue in Data Structure are:

1. **Enqueue() –** Adds (or stores) an element to the end of the queue..
2. **Dequeue() –** Removal of elements from the queue.
3. **Peek() or front()-** Acquires the data element available at the front node of the queue without deleting it.
4. **rear() –** This operation returns the element at the rear end without removing it.
5. **isFull() –** Validates if the queue is full.
6. **isNull() –** Checks if the queue is empty.

#### Types of Queue:

There are four different types of queues:

- Simple Queue
- Circular Queue
- Priority Queue
- Double Ended Queue

#### Simple Queue

In a simple queue, insertion takes place at the rear and removal occurs at the front. It strictly follows the FIFO (First in First out) rule.

#### Circular Queue

In a circular queue, the last element points to the first element making a circular link.

#### Priority Queue

A priority queue is a special type of queue in which each element is associated with a priority and is served according to its priority. If elements with the same priority occur, they are served according to their order in the queue.

#### Deque (Double Ended Queue)

In a double ended queue, insertion and removal of elements can be performed from either from the front or rear. Thus, it does not follow the FIFO (First In First Out) rule.