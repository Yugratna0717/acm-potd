Q. Given a string s of lower and upper case English letters.  

A good string is a string which doesn't have two adjacent characters s[i] and s[i + 1] where:  

0 <= i <= s.length - 2  
s[i] is a lower-case letter and s[i + 1] is the same letter but in upper-case or vice-versa.  
To make the string good, you can choose two adjacent characters that make the string bad and remove them. You can keep doing this until the string becomes good.  

Return the string after making it good. The answer is guaranteed to be unique under the given constraints.  

Notice that an empty string is also good.   


  
ANS:  
  
string st;  
    for (char c : s) {  
        if (!st.empty()&&abs(st.back()-c)==32) st.pop_back();  
        else st+=c;  
    }  
    return st;  
<img width="1468" height="764" alt="image" src="https://github.com/user-attachments/assets/5a451ba8-9241-417e-9f46-865417bff9f0" />


