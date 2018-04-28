* # �������
Given a binary tree, find its maximum depth.

The maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.
����һ�����������ҳ��������ȡ�

�����������Ϊ���ڵ㵽��ԶҶ�ӽڵ���·���ϵĽڵ�����
* # ���ʵ��
```c
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    int maxDepth(TreeNode* root) {
        if (root == NULL)
            return 0;
        
        int m = maxDepth(root->left) + 1;
        int n = maxDepth(root->right) + 1;

        if(m>n)
            return m;
        else 
            return n;
    }
};
```
* # �ܽ����
�õݹ�ķ��������������У�������������������������ȡ�