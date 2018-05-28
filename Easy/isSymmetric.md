* # �������
Given a binary tree, check whether it is a mirror of itself ��
����һ�������� ���ж��Ƿ�Ϊ����Գơ�
* # ���ʵ��

```c
class Solution {
public:
    bool isSymmetric(TreeNode* root) {
        
     if(root == NULL)
        return true;
         
            return symmetric(root->left,root->right);
    }
    
    bool symmetric(TreeNode* left,TreeNode* right){
            if(left == NULL && right == NULL)
                return true;
            if(left == NULL || right == NULL)
                return false;
            return (left->val==right->val)&&symmetric(left->left,right->right)&&symmetric(left->right,right->left);
        }
};
```
* # �ܽ����
 �õݹ�ķ������ж�left->left==right->right���Լ�left->right==right->left��