Q. Given the root of a binary tree, return its maximum depth.  
  
A binary tree's maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.  

ANS:  

class Solution {  
public:  
    int maxDepth(TreeNode* root) {  
        if (!root) return 0;  
        return 1 + max(maxDepth(root->left), maxDepth(root->right));  
    }  
};  

<img width="1448" height="749" alt="image" src="https://github.com/user-attachments/assets/c8e50c13-cf6f-4a70-b964-7dd188293476" />


