
* # �������
���дһ��������ʹ�����ɾ��ĳ�������и����ģ���ĩβ�ģ��ڵ㣬����ֻ������Ҫ��ɾ���Ľڵ㡣

* # ���ʵ��
 ```c
 /**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution(object):
    def deleteNode(self, node):
        """
        :type node: ListNode
        :rtype: void Do not return anything, modify node in-place instead.
        """
        
        node.val = node.next.val
        node.next = node.next.next


```c
class Solution {
public:
    void deleteNode(ListNode* node) {
      
        node->val=node->next->val;
        node->next=node->next->next;
    }
    
};
```

```
* # �ܽ����
 
���¸��ڵ㸳��Ҫɾ���Ľڵ㣬Ȼ��ɾ����һ���ڵ㼴�ɡ�
