 int rangeSumBST(TreeNode* root, int low, int high) {
        if (!root) {
            return 0;
        }
        int rootVal=root->val ;
        int currVal = (root->val >= low && root->val <= high) ? rootVal : 0;
        
        int leftSum = rangeSumBST(root->left, low, high);
        int rightSum = rangeSumBST(root->right, low, high);
        
        return currVal + leftSum + rightSum;
    }
