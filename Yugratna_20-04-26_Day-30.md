Q. Given an integer n, return true if it is a power of two. Otherwise, return false.  
An integer n is a power of two, if there exists an integer x such that n == 2^x.  
  
ANS:  
  
class Solution {  
public:  
    bool isPowerOfTwo(int n) {  
        return n > 0 && (n & (n-1)) == 0;  
    }  
};  
<img width="1445" height="757" alt="image" src="https://github.com/user-attachments/assets/96597318-d66f-4cfb-976f-e91c21850c9d" />
