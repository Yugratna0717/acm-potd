#Solution pasted from leetcode:
class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
       int n= nums.size();
       int i=0;
       for(int j=1; j<n; j++){
        if(nums[i]!=nums[j]){
            nums[i+1]= nums[j];
            i++;
        }
       }
       return i+1; 
    }
};
<img width="1445" height="749" alt="image" src="https://github.com/user-attachments/assets/1922269e-2a1f-4d5b-81ac-fcb68bd05798" />

