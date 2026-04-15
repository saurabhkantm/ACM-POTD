class Solution {
public:
    int maxDepth(TreeNode* root) {

        if(root == nullptr) return 0;
        return 1 + max(maxDepth(root->left), maxDepth(root->right));
        
    }
};
<img width="1909" height="858" alt="image" src="https://github.com/user-attachments/assets/d81131a0-a669-468b-96f6-46f6b0c8cd46" />
