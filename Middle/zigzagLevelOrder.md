* # �������
Given a binary tree, return the zigzag level order traversal of its nodes' values. (ie, from left to right, then right to left for the next level and alternate between).
����һ����������������ڵ�ֵ�ľ���β�α����������ȴ������ң��ٴ������������һ��������Դ����ƣ������֮�佻����У���
* # ���ʵ��
```c
class Solution {
public:

    vector<vector<int> > zigzagLevelOrder(TreeNode *root) {  
    vector<vector<int> > vec;  
        if(root == NULL)  
            return vec;  
        queue<TreeNode *> q;  
        q.push(root);  
        int flag = 0;
        while(!q.empty()){   
            TreeNode *p;  
            vector<int> sub;  
            int l = q.size(); 
            while(l--){  
                 p = q.front();  
                 q.pop();  
                 if(p->left) 
                     q.push(p->left);  
                 if(p->right) 
                     q.push(p->right);  
                 sub.push_back(p->val);  
            }  
            if(flag%2 != 0){     
                reverse(sub.begin(),sub.end());     
            }  
            vec.push_back(sub);  
            flag++; 
        }  
        return vec;  
    }  
};
```
* # �ܽ����
 ��bfs��⣬��flagʵ�־�ݲ�α�������reverseʵ�ִ��ҵ��������