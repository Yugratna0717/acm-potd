Q. A valid parentheses string is either empty "", "(" + A + ")", or A + B, where A and B are valid parentheses strings, and + represents string concatenation.  
  
For example, "", "()", "(())()", and "(()(()))" are all valid parentheses strings.  
  
A valid parentheses string s is primitive if it is nonempty, and there does not exist a way to split it into s = A + B,  
with A and B nonempty valid parentheses strings.  
  
Given a valid parentheses string s, consider its primitive decomposition: s = P1 + P2 + ... + Pk, where Pi are primitive valid parentheses strings.  
  
Return s after removing the outermost parentheses of every primitive string in the primitive decomposition of s.  

ANS:  
  
class Solution {  
public:  
    string removeOuterParentheses(string s) {  
        string result="";  
        int cnt=0;  
        for(char ch:s){  
            if(ch=='('){  
                if(cnt>0) result+=ch;  
                cnt++;  
            }  
            else if(ch==')'){  
                cnt--;  
                if(cnt>0) result+=ch;  
            }  
        }  
        return result;  
    }    
};  

<img width="1465" height="772" alt="image" src="https://github.com/user-attachments/assets/538de431-383e-42a0-a1bb-86eef0f6536c" />
