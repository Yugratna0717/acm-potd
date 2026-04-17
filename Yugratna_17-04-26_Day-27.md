Q. Given the root of a binary tree, return the length of the diameter of the tree.  

The diameter of a binary tree is the length of the longest path between any two nodes in a tree. This path may or may not pass through the root.  

The length of a path between two nodes is represented by the number of edges between them.  
  
ANS:  
  
class Solution {  
public:  
    int diameterOfBinaryTree(TreeNode* root) {  
        int ans=0;  
        function<int(TreeNode*)> h=[&](TreeNode* node)->int{  
        if(!node)return 0;  
        int l=h(node->left),r=h(node->right);  
        ans=max(ans,l+r); return 1+max(l,r);  
        };  
        h(root); return ans;  
    }  
};  
<img width="1447" height="756" alt="image" src="https://github.com/user-attachments/assets/ac4eded3-ab58-4ff4-9f49-f096b7947716" />
