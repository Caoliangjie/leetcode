* # �������
Given a singly linked list, determine if it is a palindrome.

����һ�������Ƿ�Ϊ��������

* # ���ʵ��
```c
class Solution {
public:
    bool isPalindrome(ListNode* head) {
     ListNode *fast=head,*slow=head;
     stack<ListNode*> s;
    
     while(fast != NULL && fast->next != NULL)
     {
         s.push(slow);
         slow = slow->next;
         fast = fast->next->next;
     }
     if(fast !=NULL)
     {
         slow=slow->next;
     }
     while(slow!=NULL)
     {
         if(slow->val!=s.top()->val)
             return false;
         s.pop();
         slow = slow->next;
     }
        return true;
    }
};
```
```python
class Solution:
    def isPalindrome(self, head):

        stk = []
        slow,fast = head, head
        while fast and fast.next:

            stk.append(slow)
            slow = slow.next
            fast = fast.next.next

        if fast != None:

            slow = slow.next

        while slow:
            tmp = stk.pop()
            if tmp.val != slow.val:
                return False
            slow = slow.next
            
        return True
```
* # �ܽ����
 ����һ����ָ���һ����ָ�룬�������ǰ�벿�ֽ�����ջ�У�Ȼ�����벿�ֽ���������Ƚϣ�����ͬ����Ϊ��������ע������ż�������
