	#include <iostream>
	#include <cstdlib>
	class Queue {
		private:
		    int *array;
		    int front;
		    int rear;
		    int capacity;
		public:
		    Queue(int size) {
		        capacity = size;
		        array = new int[capacity];
		        front = rear = -1;
	    }
	    bool isFull() {
	        return (rear + 1) % capacity == front;
	    }
	    bool isEmpty() {
	        return front == -1;
	    }
	    void enqueue(int item) {
	        if (isFull()) {
	            std::cout << "Queue is full. Cannot enqueue." << std::endl;
	            return;
	        }
	        if (isEmpty()) {
	            front = 0;
	        }
	        rear = (rear + 1) % capacity;
	        array[rear] = item;
	    }
	    int dequeue() {
	        if (isEmpty()) {
	            std::cout << "Queue is empty. Cannot dequeue." << std::endl;
	            return -1; // You can return a special value to indicate an error
	        }
	        int item = array[front];
	        if (front == rear) {
	            front = rear = -1;
	        } else {
	            front = (front + 1) % capacity;
	        }
	        return item;
	    }
	    int peek() {
	        if (isEmpty()) {
	            std::cout << "Queue is empty. Cannot peek." << std::endl;
	            return -1; // You can return a special value to indicate an error
	        }
	        return array[front];
	    }
	};
	int main() {
	    Queue queue(5);
	    queue.enqueue(1);
	    queue.enqueue(2);
	    queue.enqueue(3);
	    queue.enqueue(4);
	    queue.enqueue(5);
	    std::cout << "Front of the queue: " << queue.peek() << std::endl;
	    while (!queue.isEmpty()) {
	        std::cout << "Dequeued: " << queue.dequeue() << std::endl;
	    }
	    return 0;
	}
