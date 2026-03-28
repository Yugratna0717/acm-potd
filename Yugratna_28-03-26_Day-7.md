Q. Given an integer array nums, rotate the array to the right by k steps, where k is non-negative.  

ANS:  

class Solution {  
public:  
    void rotate(vector<int>& nums, int k) {  
    
       int n = nums.size();  
       
        k = k % n;  

        reverse(nums.begin(), nums.end());  
        reverse(nums.begin(), nums.begin() + k);  
        reverse(nums.begin() + k, nums.end());  
    }  
};   

<img width="1447" height="750" alt="image" src="https://github.com/user-attachments/assets/710f548d-6ad9-4677-b97b-3d225b0f3164" />
