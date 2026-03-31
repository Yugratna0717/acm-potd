Q. Given the head of a singly linked list, return the middle node of the linked list.  

If there are two middle nodes, return the second middle node.  

ANS:  

class Solution {  
public:  
    ListNode* middleNode(ListNode* head) {  
        ListNode* slow = head, *fast = head;  
        while (fast && fast->next) {  
            slow = slow->next;  
            fast = fast->next->next;  
        }  
        return slow;  
    }  
};  

<img width="1465" height="765" alt="image" src="https://github.com/user-attachments/assets/d5a0910c-6767-444a-a5db-de9cbdf5bd0a" />


