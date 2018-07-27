* # �������
Given a binary tree, return the level order traversal of its nodes' values. (ie, from left to right, level by level).
����һ���������������䰴��α����Ľڵ�ֵ�� �������أ������ҷ������нڵ㣩��
* # ���ʵ��
```c
class Solution {
public:
    vector<vector<int>> levelOrder(TreeNode* root) {
         vector<vector<int>> vec;
        if(!root) return vec;
        queue<TreeNode*> q;
        q.push(root);
        while(!q.empty())
        {   
            vector<int> tmp;
            int l = q.size();
            for(;l>0;l--)
            {
                TreeNode* t;
                t = q.front();
                tmp.push_back(t->val);
                q.pop();
                if(t->left) q.push(t->left);
                if(t->right) q.push(t->right);
            }
            vec.push_back(tmp);
          }
        
        return vec;
    }
};
class Solution:
    def levelOrder(self, root):
        """
        :type root: TreeNode
        :rtype: List[List[int]]
        """

        if not root  :
            return []
        res,cur_level = [],[root]
        while cur_level:
            next_level ,temp_level = [],[]      
            for node in cur_level:
                if node.left: 
                    next_level.append(node.left)
                if node.right:
                    next_level.append(node.right)
                temp_level.append(node.val)
            cur_level = next_level
            res.append(temp_level)
        
        return res
```
* # �ܽ����
   �ù��������������ÿ����㲻Ϊ�գ�����ֵ��������vec�����ҳ��У�ͬʱ�������ӽ�����У�ѭ����
