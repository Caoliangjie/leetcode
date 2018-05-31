
* # �������
Given an array where elements are sorted in ascending order, convert it to a height balanced BST.

For this problem, a height-balanced binary tree is defined as a binary tree in which the depth of the two subtrees of every node never differ by more than 1.
��һ�������������е��������飬ת��Ϊһ�ø߶�ƽ�������������

�����У�һ���߶�ƽ���������ָһ��������ÿ���ڵ� ���������������ĸ߶Ȳ�ľ���ֵ������ 1��

ʾ��:
* # ���ʵ��
class Solution {  
public:  
    TreeNode *sortedArrayToBST(vector<int> &num)  
    {  
        return bst(num , 0 , num.size() - 1);  
    }  
    //ʹ�ö��ַ�����ƽ�����������  
    TreeNode *bst(vector<int> &num , int left , int right)  
    {  
        //�ݹ��������  
        if(left > right)  
            return NULL;  
        int mid = (left + right)/2;  
        TreeNode *root = new TreeNode(num[mid]);//����㣬Ϊ��ǰ������м�ֵ  
        root->left = bst(num , left , mid - 1);//����������Ϊ����������м�ֵ  
        root->right = bst(num , mid + 1 , right);//�������Һ���Ϊ�Ұ��������м�ֵ  
        return root;  
    }  
};  

* # �ܽ����
�����п�֪ƽ�����������ص㣬����ƽ������������ĸ��ڵ��ֵǡ��ʱ���нڵ�ֵ���м�ֵ�����ڵ������Ϊż���������ǿ�ǰ�Ǹ����ö��ֲ��ҵķ�ʽ���Ƚ��м�ڵ���Ϊ���ڵ㣬���ڵ��������Ϊ����������м�ֵ��������Ϊ�Ұ�νڵ���м�ֵ��
