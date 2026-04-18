Q. Given the roots of two binary trees root and subRoot, r  
eturn true if there is a subtree of root with the same structure and node values of subRoot and false otherwise.  
  
A subtree of a binary tree tree is a tree that consists of a node in tree and all of this node's descendants.   
The tree tree could also be considered as a subtree of itself.  
  
ANS:    
  
class Solution {  
public:  
    bool isSubtree(TreeNode* root, TreeNode* sub) {  
    if (!root) return false;  
    if (isSame(root,sub)) return true;  
    return isSubtree(root->left,sub)||isSubtree(root->right,sub);  
}  
bool isSame(TreeNode* s,TreeNode* t){  
    if(!s&&!t)return true; if(!s||!t)return false;  
    return s->val==t->val&&isSame(s->left,t->left)&&isSame(s->right,t->right);  
}  
};  
<img width="1461" height="754" alt="image" src="https://github.com/user-attachments/assets/3cc59168-e1d2-4d1a-8ca4-caa95a8384eb" />
