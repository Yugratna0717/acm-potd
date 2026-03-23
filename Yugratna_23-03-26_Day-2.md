Q. Given an array of integers nums and an integer k, return the total number of subarrays whose sum equals to k.

A subarray is a contiguous non-empty sequence of elements within an array.

SOLUTION:

class Solution {    
public:  
    int subarraySum(vector<int>& nums, int k) {  
        map<int,int>mpp;  
        mpp[0]=1;  
        int preSum=0;  
        int cnt=0;  
        int n= nums.size();  
        for(int i=0; i<n; i++){  
            preSum+=nums[i];  
            int remove= preSum-k;  
            cnt+=mpp[remove];  
            mpp[preSum]+=1;  
        }  
        return cnt;  
    }  
};  

<img width="1457" height="758" alt="image" src="https://github.com/user-attachments/assets/bcccd69c-946c-4b04-b0ed-7374096d8eb4" />

