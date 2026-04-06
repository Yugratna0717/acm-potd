Q. Implement a first in first out (FIFO) queue using only two stacks. The implemented queue should support all the functions of   
a normal queue (push, peek, pop, and empty).  

Implement the MyQueue class:  

i. void push(int x) Pushes element x to the back of the queue.  
ii. int pop() Removes the element from the front of the queue and returns it.  
iii. int peek() Returns the element at the front of the queue.  
iv. boolean empty() Returns true if the queue is empty, false otherwise.  

ANS:    

class MyQueue {  
private:  
    stack<int> incoming, outgoing;  
    
public:  
    MyQueue() {}  
    
    void push(int x) {  
        incoming.push(x);  
    }  
    
    int pop() {  
        peek();  
        int res = outgoing.top();  
        outgoing.pop();   
        return res;  
    }  
    
    int peek() {  
        if (outgoing.empty()) {  
            while (!incoming.empty()) {  
                outgoing.push(incoming.top());  
                incoming.pop();  
            }  
        }  
        return outgoing.top();  
    }  
    
    bool empty() {  
        return incoming.empty() && outgoing.empty();  
    }  
};  

<img width="1466" height="762" alt="image" src="https://github.com/user-attachments/assets/85c382f2-d3b2-4d18-bbc5-50f12c4e4510" />
