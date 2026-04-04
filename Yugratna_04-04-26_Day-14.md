Q. Given the head of a singly linked list, return true if it is a palindrome or false otherwise.  

ANS:-  

class Solution {  
public:  
    bool isPalindrome(ListNode* head) {  
        if (!head || !head->next) return true;  
        
        ListNode* slow = head, *fast = head;  
        while (fast && fast->next) {  
            slow = slow->next;  
            fast = fast->next->next;  
        }  
        
        ListNode* prev = nullptr;  
        while (slow) {  
            ListNode* next = slow->next;  
            slow->next = prev;  
            prev = slow;   
            slow = next;  
        }  
        
        ListNode* left = head, *right = prev;  
        while (right) {  
            if (left->val != right->val) return false;  
            left = left->next;  
            right = right->next;  
        }  
        return true;  
    }  
};  

<img width="1469" height="769" alt="image" src="https://github.com/user-attachments/assets/e6b2c43c-ed5a-41c7-a92d-649725aceae6" />
