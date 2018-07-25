* # �������
Given a linked list, determine if it has a cycle in it.<br/>
����һ�������ж����Ƿ�Ϊѭ������

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
    bool hasCycle(ListNode *head) {
        ListNode* fast = head;
        ListNode* slow = head;
        while(fast && fast->next)
        {
            fast = fast->next->next;
            slow = slow->next;
            if(slow == fast)
                return true;
        }
        return false;
    }
};
class Solution(object):
    def hasCycle(self, head):
        """
        :type head: ListNode
        :rtype: bool
        """
        slow,fast = head, head
        while fast and fast.next:
            slow = slow.next
            fast = fast.next.next
            if slow == fast:
                return True
        
        return False
```
* # �ܽ����
  ��������ָ�룬һ��Ϊ��ָ�룬һ��Ϊ��ָ�룬��ָ���ߵ��ٶ�����ָ���������������ָ���ܹ��ٴ���������˵����������һ��ѭ������
