
* # �������
Given a binary tree, return the inorder traversal of its nodes' values.
����һ���������������������� ������
* # ���ʵ��

```c
class Solution {
public:
    vector<int> vec;
    vector<int> inorderTraversal(TreeNode* root) {
        if(root != NULL)
        {
            inorderTraversal(root->left);
            vec.push_back(root->val);
            inorderTraversal(root->right);
            return vec;
        }
        return vec;
    }
};
```

* # �ܽ����
 ������������Ĺ����õݹ�ķ�ʽ��⡣