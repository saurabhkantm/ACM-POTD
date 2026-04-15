class Solution {
public:
    TreeNode* invertTree(TreeNode* root) {
       if(!root) return 0;
      swap(root->left,root->right);
       invertTree(root->left);
       invertTree(root->right);
       return root;
    }
};
<img width="1900" height="857" alt="image" src="https://github.com/user-attachments/assets/c3cbeda2-b150-4601-9dea-d8baff3c9e38" />
