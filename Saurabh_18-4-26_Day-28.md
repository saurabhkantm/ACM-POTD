class Solution {
public:
    TreeNode* buildTree(vector<int>& preorder, vector<int>& inorder) 
    {
        unordered_map<int, int> mpp;

        for(int i=0; i<inorder.size(); i++)
        {
            mpp[inorder[i]]=i;
        }

        return buildTree(preorder, 0, preorder.size()-1, inorder, 0, inorder.size()-1, mpp);
    }

    TreeNode* buildTree(vector<int>& preorder, int ps, int pe, vector<int>& inorder, int is, int ie, unordered_map<int, int>& mpp)
    {
        if(ps>pe || is>ie) return NULL;

        TreeNode* nn = new TreeNode(preorder[ps]);

        int root_val = mpp[nn->val];
        int left_data = root_val - is;

        nn->left = buildTree(preorder, ps+1, ps+left_data, inorder, is, root_val-1, mpp);
        nn-> right = buildTree(preorder, ps+left_data+1, pe, inorder, root_val+1, ie, mpp);

        return nn;
    }
};
<img width="1883" height="792" alt="image" src="https://github.com/user-attachments/assets/81094556-19a6-4c66-a065-0e9db571d8bb" />
