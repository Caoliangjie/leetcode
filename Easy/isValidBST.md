* # �������
����һ�����������ж����Ƿ���һ����Ч�Ķ�����������
* # ���ʵ��
```c
class Solution {
public:
    bool isValidBST(TreeNode* root) {
        if(root == NULL)
            return true;
        stack<TreeNode*> st;
        TreeNode *pre = NULL;

        while(root || !st.empty())
        {
            if(root)
            {
                st.push(root);
                root = root->left;
            }
            else
            {
                root = st.top();
                st.pop();
                if(pre && (root->val <= pre->val))
                    return false;
                pre = root;
                root = root->right;
            }
        }
        return true;
    }
};
```
* # �ܽ����
 ��Ϊ�������������������������ģ�����Ҫ��֤�������Ƿ�Ϊ������������
����������������������ǰһ������ֵ���ڵ�ǰ����ֵ����֤��������Ƕ�����������