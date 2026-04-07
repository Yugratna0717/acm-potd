Q Implement a last-in-first-out (LIFO) stack using only two queues. The implemented stack should support all the functions of a normal stack  
(push, top, pop, and empty).  

Implement the MyStack class:  

I. void push(int x) Pushes element x to the top of the stack.  
II. int pop() Removes the element on the top of the stack and returns it.  
III. int top() Returns the element on the top of the stack.  
IV. boolean empty() Returns true if the stack is empty, false otherwise.  


ANS:  

class MyStack {  
private:  
    queue<int> q;  
    
public:  
    MyStack() {}  
    
    void push(int x) {  
        q.push(x);  
        for (int i = 1; i < q.size(); i++) {  
            q.push(q.front());  
            q.pop();  
        }  
    }  
    
    int pop() {  
        int res = q.front();  
        q.pop();  
        return res;  
    }  
    
    int top() {  
        return q.front();  
    }  
    
    bool empty() {  
        return q.empty();  
    }  
};  
<img width="1464" height="765" alt="image" src="https://github.com/user-attachments/assets/c6bbe583-49be-4d37-8bfb-2cd160a1b2ee" />

