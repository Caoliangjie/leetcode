
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
```c
class Solution {
public:
    vector<int> inorderTraversal(TreeNode* root) {      
        TreeNode *p;
        stack<TreeNode*> stk;
        vector<int> vec;
        p = root;
        while (p != NULL || !stk.empty())
        {
            while (p != NULL)
            {
                stk.push(p);
                p = p->left;
            }
            
            if (!stk.empty())
            {
                p = stk.top();
                stk.pop();
                vec.push_back(p->val);
                p = p->right;
            }
        }
        
        return vec;
    }
};
```
* # �ܽ����
 ������������Ĺ����õݹ�ķ�ʽ��⡣�ڶ��֣��÷ǵݹ�ķ�ʽ��⡣