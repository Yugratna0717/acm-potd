Q. You are given the heads of two sorted linked lists list1 and list2.  

Merge the two lists into one sorted list. The list should be made by splicing together the nodes of the first two lists.  

Return the head of the merged linked list.  

ANS:  

class Solution {  
public:  
    ListNode* mergeTwoLists(ListNode* list1, ListNode* list2) {  
        ListNode* dummy = new ListNode(0);    
        ListNode* current = dummy;  
        
        while (list1 && list2) {  
            if (list1->val <= list2->val) {  
                current->next = list1;  
                list1 = list1->next;  
            } else {  
                current->next = list2;  
                list2 = list2->next;  
            }  
            current = current->next;  
        }  
        
        current->next = list1 ? list1 : list2;  
        return dummy->next;  
    }  
};  

<img width="1462" height="759" alt="image" src="https://github.com/user-attachments/assets/d5dfb42e-1ab5-48fd-915e-b1cac7641c43" />
