Q. You are given a string s consisting of lowercase English letters. A duplicate removal consists of choosing two adjacent and equal letters and removing them.  

We repeatedly make duplicate removals on s until we no longer can.  

Return the final string after all such duplicate removals have been made. It can be proven that the answer is unique.  

ANS:  
class Solution {  
public:  
    string removeDuplicates(string s) {  
        string st = "";  
        for (char c : s) {  
            if (!st.empty() && st.back() == c) {  
                st.pop_back();  
            } else {  
                st.push_back(c);  
            }  
        }  
        return st;  
    }  
};  
<img width="1465" height="766" alt="image" src="https://github.com/user-attachments/assets/94748f19-ea84-4fd0-908e-5a3b9781b11e" />
