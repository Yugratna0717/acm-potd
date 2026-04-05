Q. Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.  

An input string is valid if:  

i) Open brackets must be closed by the same type of brackets.  
ii) Open brackets must be closed in the correct order.  
iii) Every close bracket has a corresponding open bracket of the same type.  


ANS:

class Solution {  
public:  
    bool isValid(string s) {  
        stack<char> st;  

        for(char c : s) {  
            if(c == '(' || c == '[' || c == '{') {  
                st.push(c);  
            }   
            else {  
                if(st.empty()) return false;  

                char top = st.top();  
                if((c == ')' && top == '(') ||  
                   (c == ']' && top == '[') ||  
                   (c == '}' && top == '{')) {  
                    st.pop();  
                } else {  
                    return false;  
                }  
            }  
        }  

        return st.empty();  
    }  
};  
