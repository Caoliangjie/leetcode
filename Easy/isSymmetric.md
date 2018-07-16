* # �������
Given a binary tree, check whether it is a mirror of itself ��
����һ�������� ���ж��Ƿ�Ϊ����Գơ�
* # ���ʵ��

```c
class Solution {
public:
    bool isSymmetric(TreeNode* root) {
        if(!root)
        return true;  
        return checkSymmetric(root->left,root->right);
    }
    
    bool checkSymmetric(TreeNode* left,TreeNode* right){
            if(!left && !right)
                return true;
            if(!left || !right)
                return false;
            return checkSymmetric(left->left,right->right)&&checkSymmetric(left->right,right->left)&&(left->val==right->val); 
        }
};
```
* # �ܽ����
 �õݹ�ķ������ж�left->left==right->right���Լ�left->right==right->left��
