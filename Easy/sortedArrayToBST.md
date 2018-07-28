* # �������
Given an array where elements are sorted in ascending order, convert it to a height balanced BST.

For this problem, a height-balanced binary tree is defined as a binary tree in which the depth of the two subtrees of every node never differ by more than 1.
��һ�������������е��������飬ת��Ϊһ�ø߶�ƽ�������������

�����У�һ���߶�ƽ���������ָһ��������ÿ���ڵ� ���������������ĸ߶Ȳ�ľ���ֵ������ 1��

ʾ��:
* # ���ʵ��
```c
class Solution {
public:  
    TreeNode* sortedArrayToBST(vector<int>& nums) {
        return  bst(nums, 0 , nums.size()-1 );
    }
    
    TreeNode* bst(vector<int>& nums , int left, int right){
        if(left > right) return NULL;
        int mid = (left+right)/2; 
        TreeNode *root = new TreeNode(nums[mid]); //����㣬Ϊ��ǰ�����м�ֵ
        root->left = bst(nums, left, mid-1); //����������Ϊ����������м�ֵ
        root->right = bst(nums, mid+1, right); //�������Һ���Ϊ�Ұ��������м�ֵ
        
         return root;
    }  
};  
class Solution:    
    def bst(self,left,right,nums):
        if left > right:    
            return None
        mid = left + (right-left)//2
        root = TreeNode(nums[mid])

        root.left = self.bst(left,mid-1,nums)
        root.right = self.bst(mid+1,right,nums)

        return root   
    def sortedArrayToBST(self, nums):
        """
        :type nums: List[int]
        :rtype: TreeNode
        """
        return self.bst(0,len(nums)-1,nums)
```
* # �ܽ����
�����п�֪ƽ�����������ص㣬����ƽ������������ĸ��ڵ��ֵǡ��ʱ���нڵ�ֵ���м�ֵ�����ڵ������Ϊż���������ǿ�ǰ�Ǹ����ö��ֲ��ҵķ�ʽ���Ƚ��м�ڵ���Ϊ���ڵ㣬���ڵ��������Ϊ����������м�ֵ��������Ϊ�Ұ�νڵ���м�ֵ��
