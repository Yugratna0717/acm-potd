Q. Given an array arr of integers, check if there exist two indices i and j such that :  

i != j  
0 <= i, j < arr.length  
arr[i] == 2 * arr[j]  

ANS:  

class Solution {  

public:  

    bool checkIfExist(vector<int>& arr) {  
    
        unordered_set<int> st;  
        
        for (int num : arr) {  
        
            if (st.count(2 * num) || (num % 2 == 0 && st.count(num / 2))) {  
            
                return true;  
                
            }  
            st.insert(num);  
        }  
        return false;  
    }  
};  
<img width="1446" height="752" alt="image" src="https://github.com/user-attachments/assets/89a68075-df45-4817-92d8-e3bb0bd50cae" />
