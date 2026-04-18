class Solution {
public:
    int diameter=0;
    int check(TreeNode* root)
    {
        if(root == nullptr) return 0;

        int leftheight = check(root->left);
        int rightheight = check(root->right);

        diameter = max(diameter, leftheight + rightheight);

        return 1+ max(leftheight, rightheight);
    }
    int diameterOfBinaryTree(TreeNode* root) {

        check(root);
        return diameter;
        
    }
};
<img width="1815" height="847" alt="image" src="https://github.com/user-attachments/assets/dce3b6c4-0687-4294-81e7-0720d15bf817" />
