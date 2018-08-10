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
```python
class Solution:  
    def symmertric(self,left,right):
        if left == None and right==None:
            return True
        if left == None or right==None:
            return False

        return (left.val == right.val) and self.symmertric(left.left,right.right) and self.symmertric(left.right,right.left)

    
    def isSymmetric(self, root):
        """
        :type root: TreeNode
        :rtype: bool
        """
        if root == None :
            return True
        return self.symmertric(root.left,root.right)
```
* # �ܽ����
 �õݹ�ķ������ж�left->left==right->right���Լ�left->right==right->left��
