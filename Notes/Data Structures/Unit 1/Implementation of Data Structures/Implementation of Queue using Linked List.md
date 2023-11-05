	#include <iostream>
	class Node {
	public:
	    int data;
	    Node* next;
	    Node(int value) : data(value), next(nullptr) {
	    }
	};
	class Queue {
	private:
	    Node* front;
	    Node* rear;
	public:
	    Queue() : front(nullptr), rear(nullptr) {
	    }
	    bool isEmpty() {
	        return front == nullptr;
	    }
	    void enqueue(int value) {
	        Node* newNode = new Node(value);
	        if (rear == nullptr) {
	            front = rear = newNode;
	        } else {
	            rear->next = newNode;
	            rear = newNode;
	        }
	    }
	    int dequeue() {
	        if (isEmpty()) {
	            std::cout << "Queue is empty. Cannot dequeue." << std::endl;
	            return -1; // You can return a special value to indicate an error
	        }
	        Node* temp = front;
	        int value = front->data;
	        front = front->next;
	        if (front == nullptr) {
	            rear = nullptr;
	        }
	        delete temp;
	        return value;
	    }
	    int peek() {
	        if (isEmpty()) {
	            std::cout << "Queue is empty. Cannot peek." << std::endl;
	            return -1; // You can return a special value to indicate an error
	        }
	        return front->data;
	    }
	};
	int main() {
	    Queue queue;
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
