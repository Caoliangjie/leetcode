* # �������
Merge two sorted linked lists and return it as a new list. 
The new list should be made by splicing together the nodes of the first two lists.<br/><br/>

��������������ϲ�Ϊһ���µ������������ء���������ͨ��ƴ�Ӹ�����������������нڵ���ɵġ�


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
class Solution {
public:
    ListNode* mergeTwoLists(ListNode* l1, ListNode* l2) {
        
        if(l1 == NULL)
            return l2;
        else if(l2 == NULL)
            return l1;
        ListNode* qMerge = NULL;
        if(l1->val <= l2->val)
        {
            qMerge = l1;
            qMerge->next = mergeTwoLists(l1->next,l2);
        }
        else
        {
            qMerge = l2;
            qMerge->next = mergeTwoLists(l1,l2->next);
        }
        
        return qMerge;

    }
};
```

* # �ܽ����
 1.��������l1Ϊ���򷵻�l2��l2Ϊ����l1��<br/>
 2.�Ƚ����������һ�����Ĵ�С��qMergeΪ�ºϲ��������ͷ�ڵ㡣<br/>
 3.ȷ��ͷ�ڵ����ʣ�µĽ���У�ѡ����һ�����ȥ���ӵ��ڶ���ѡ���Ľ����棬Ȼ�󲻶��ظ���ֱ������Ϊ�ա�