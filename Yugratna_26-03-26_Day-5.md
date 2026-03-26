Q. Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.  

Note that you must do this in-place without making a copy of the array.  

ANS:  

class Solution {  
public:  
    void moveZeroes(vector<int>& nums) {  
       int j= -1;  
       int n= nums.size();  
       for(int i=0; i<n; i++){  
        if(nums[i]==0){  
            j=i;  
            break;  
        }  
       }  
       if(j==-1) return;  
       for(int i=j+1; i<n; i++){  
        if(nums[i]!=0){  
            swap(nums[i],nums[j]);  
            j++;  
        }  
       }  
       
    }  
};  

<img width="1448" height="744" alt="image" src="https://github.com/user-attachments/assets/b0a82b88-cdc4-44f2-af0a-0fbe66fc5ef1" />
