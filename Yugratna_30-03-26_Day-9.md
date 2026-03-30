Q. Given head, the head of a linked list, determine if the linked list has a cycle in it.  
There is a cycle in a linked list if there is some node in the list that can be reached again by continuously following the next pointer.   
Internally, pos is used to denote the index of the node that tail's next pointer is connected to. Note that pos is not passed as a parameter.  
Return true if there is a cycle in the linked list. Otherwise, return false.  

ANS:  
class Solution {  
public:  
    bool hasCycle(ListNode *head) {  
        if (!head) return false;  
        ListNode *slow = head, *fast = head;  
        while (fast && fast->next) {  
            slow = slow->next;  
            fast = fast->next->next;  
            if (slow == fast) return true;  
        }  
        return false;  
    }  
};  

<img width="1467" height="760" alt="image" src="https://github.com/user-attachments/assets/6d7c5f73-4d79-4f63-be22-365104f0e6e1" />


