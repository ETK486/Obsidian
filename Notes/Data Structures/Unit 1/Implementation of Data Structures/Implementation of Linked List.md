	#include <iostream>
	class Node {
	public:
	    int data;
	    Node* next;
	    Node(int value) : data(value), next(nullptr) {}
	};
	class LinkedList {
	public:
	    Node* head;
	    LinkedList() : head(nullptr) {
	    }
	    // Function to insert a new node at the end of the linked list
	    void append(int value) {
	        Node* newNode = new Node(value);
	        if (head == nullptr) {
	            head = newNode;
	        } else {
	            Node* current = head;
	            while (current->next != nullptr) {
	                current = current->next;
	            }
	            current->next = newNode;
	        }
	    }
	    // Function to display the linked list
	    void display() {
	        Node* current = head;
	        while (current != nullptr) {
	            std::cout << current->data << " -> ";
	            current = current->next;
	        }
	        std::cout << "nullptr" << std::endl;
	    }
	    // Function to delete a node by its value
	    void remove(int value) {
	        if (head == nullptr) {
	            return; // List is empty
	        }
	        if (head->data == value) {
	            Node* temp = head;
	            head = head->next;
	            delete temp;
	            return;
	        }
	        Node* current = head;
	        while (current->next != nullptr && current->next->data != value) {
	            current = current->next;
	        }
	        if (current->next == nullptr) {
	            return; // Node with the given value not found
	        }
	        Node* temp = current->next;
	        current->next = current->next->next;
	        delete temp;
	    }
	};
	int main() {
	    LinkedList list;
	    list.append(1);
	    list.append(2);
	    list.append(3);
	    list.append(4);
	    std::cout << "Original Linked List: ";
	    list.display();
	    list.remove(3);
	    std::cout << "Linked List after removing 3: ";
	    list.display();
	    return 0;
	}
