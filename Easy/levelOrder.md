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
        while(!q.empty()){
            vector<int> tmp;
            int size = q.size();
            while(size--){
                TreeNode* t = q.front();
                tmp.push_back(t->val);
                q.pop();
                if(t->left)
                    q.push(t->left);
                if(t->right)
                    q.push(t->right);
            }
            vec.push_back(tmp);
        }
        
        return vec;
    }
};
```
* # �ܽ����
   �ù��������������ÿ����㲻Ϊ�գ�����ֵ��������vec�����ҳ��У�ͬʱ�������ӽ�����У�ѭ����