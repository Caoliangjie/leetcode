* # �������

����һ�����������ж����Ƿ���һ����Ч�Ķ�����������

Given a binary tree, determine if it is a valid binary search tree (BST).
* # ���ʵ��

```c
class Solution {
public:
    bool isValidBST(TreeNode* root) {
    if(!root) return true;
    vector<int> vec;
    order(root,vec);
    for(int i=0;i<vec.size()-1;i++)
   {
     if(vec[i]>=vec[i+1])
      return false;
   }
   return true;
}
 
  void order(TreeNode* root,vector<int> & vec){
    if(!root) return;
    if(root->left) 
    order(root->left,vec);
    vec.push_back(root->val);
    if(root->right) 
    order(root->right,vec);
    }
};
```

* # �ܽ����

 ��Ϊ�������������������������ģ�����Ҫ��֤�������Ƿ�Ϊ������������
����������������������ǰһ������ֵ���ڵ�ǰ����ֵ����֤��������Ƕ�����������
