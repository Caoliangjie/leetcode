* # �������

����һ�����������ж����Ƿ���һ����Ч�Ķ�����������

Given a binary tree, determine if it is a valid binary search tree (BST).
* # ���ʵ��

```c

class Solution {
public:
    bool isValidBST(TreeNode* root) {
    if(!root) 
    return true;
    vector<int> arr;
    order(root,arr);
    for(int i=0;i<arr.size()-1;i++)
   {
     if(arr[i]>=arr[i+1])
      return false;
   }
   return true;
}
 
  void order(TreeNode* root,vector<int> & arr){
    if(!root) 
    return;
    if(root->left) 
    order(root->left,arr);
    arr.push_back(root->val);
    if(root->right) 
    order(root->right,arr);
  }

};
```

* # �ܽ����

 ��Ϊ�������������������������ģ�����Ҫ��֤�������Ƿ�Ϊ������������
����������������������ǰһ������ֵ���ڵ�ǰ����ֵ����֤��������Ƕ�����������