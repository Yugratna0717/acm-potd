Q. Given the root of a binary tree, invert the tree, and return its root.
  
ANS:  

  class Solution {  
public:  
    TreeNode* invertTree(TreeNode* root) {  
        if (!root) return nullptr;  
        swap(root->left, root->right);  
        invertTree(root->left); invertTree(root->right);  
        return root;  
    }  
    
};  
<img width="1458" height="754" alt="image" src="https://github.com/user-attachments/assets/fb821dd5-a5d1-4131-9e16-79c1d8b4db81" />
