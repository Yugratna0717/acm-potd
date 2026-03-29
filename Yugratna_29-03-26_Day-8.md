Q. Given the head of a singly linked list, reverse the list, and return the reversed list.  

ANS:  

class Solution {  
public:  
    ListNode* reverseList(ListNode* head) {  
        ListNode* prev = nullptr, *curr = head;  
        while (curr) {  
            ListNode* next = curr->next;  
            curr->next = prev;  
            prev = curr;  
            curr = next;  
        }  
        return prev;  
    }  
};  

<img width="1444" height="751" alt="image" src="https://github.com/user-attachments/assets/ce00562d-0578-4c77-a7e7-c3579d1a420b" />
