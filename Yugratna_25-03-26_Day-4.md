Q. Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array.  
ANS:  

class Solution {  
public:  
    int missingNumber(vector<int>& nums) {  
        int n= nums.size();  
        int XOR1= 0;  
        int XOR2=0;  
        for(int i=0; i<=n-1; i++){  
            XOR2=XOR2^nums[i];  
            XOR1= XOR1 ^ (i+1);  
            
        }  
        return XOR1^XOR2;  
    }  
};  

<img width="1448" height="749" alt="image" src="https://github.com/user-attachments/assets/7ba7f96b-2481-4bf3-80fb-357c1ec5337a" />
