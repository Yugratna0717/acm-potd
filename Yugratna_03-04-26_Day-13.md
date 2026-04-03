Q. Given the heads of two singly linked-lists headA and headB, return the node at which the two lists intersect.  
If the two linked lists have no intersection at all, return null.

ANS:  

class Solution {  
public:  
    ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {  
        if (!headA || !headB) return nullptr;  
        ListNode *pA = headA, *pB = headB;  
        
        while (pA != pB) {  
            pA = !pA ? headB : pA->next;  
            pB = !pB ? headA : pB->next;  
        }  
        return pA;  
    }  
};  
<img width="1457" height="759" alt="image" src="https://github.com/user-attachments/assets/bb74b294-3342-4880-9da2-5cbfcad2eb1c" />
