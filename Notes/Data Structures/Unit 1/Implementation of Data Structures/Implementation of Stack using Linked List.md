	#include <iostream>
    class Node {
    public:
        int data;
        Node* next;
        Node(int value) : data(value), next(nullptr) {
        }
    };
    class Stack {
    private:
        Node* top;
    public:
        Stack() : top(nullptr) {
        }
        bool isEmpty() {
            return top == nullptr;
        }
        void push(int value) {
            Node* newNode = new Node(value);
            newNode->next = top;
            top = newNode;
        }
        int pop() {
            if (isEmpty()) {
                std::cout << "Stack is empty. Cannot pop." << std::endl;
                return -1; // You can return a special value to indicate an error
            }
            int value = top->data;
            Node* temp = top;
            top = top->next;
            delete temp;
            return value;
        }
        int peek() {
            if (isEmpty()) {
                std::cout << "Stack is empty. Cannot peek." << std::endl;
                return -1; // You can return a special value to indicate an error
            }
            return top->data;
        }
    };
    int main() {
        Stack stack;
        stack.push(1);
        stack.push(2);
        stack.push(3);
        stack.push(4);
        stack.push(5);
        std::cout << "Top of the stack: " << stack.peek() << std::endl;
        while (!stack.isEmpty()) {
            std::cout << "Popped: " << stack.pop() << std::endl;
        }
        return 0;
    }
