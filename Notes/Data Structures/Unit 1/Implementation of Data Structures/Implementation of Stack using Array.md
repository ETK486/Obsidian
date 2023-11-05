	#include <iostream>
    #include <cstdlib>
    class Stack {
    private:
        int *array;
        int top;
        int capacity;
    public:
        Stack(int size) {
            capacity = size;
            array = new int[capacity];
            top = -1;
        }
        bool isFull() {
            return top == capacity - 1;
        }
        bool isEmpty() {
            return top == -1;
        }
        void push(int item) {
            if (isFull()) {
                std::cout << "Stack is full. Cannot push." << std::endl;
                return;
            }
            array[++top] = item;
        }
        int pop() {
            if (isEmpty()) {
                std::cout << "Stack is empty. Cannot pop." << std::endl;
                return -1; // You can return a special value to indicate an error
            }
            return array[top--];
        }
        int peek() {
            if (isEmpty()) {
                std::cout << "Stack is empty. Cannot peek." << std::endl;
                return -1; // You can return a special value to indicate an error
            }
            return array[top];
        }
    };
    int main() {
        Stack stack(5);
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
