* # �������
Given a singly linked list, determine if it is a palindrome.

����һ�������Ƿ�Ϊ��������

* # ���ʵ��
```c
class Solution {
public:
    bool isPalindrome(ListNode* head) {
     ListNode *fast,*slow;
     fast = slow = head;
     stack<ListNode*> s;
    
     while(fast != NULL && fast->next != NULL)
     {
         s.push(slow);
         fast = fast->next->next;
         slow = slow->next;
     }
     if(fast !=NULL)
     {
         slow=slow->next;
     }
     while(slow)
     {
         if(slow->val!=s.top()->val)
             return false;
         slow = slow->next;
         s.pop();
     }
        return true;
    }
};
```
* # �ܽ����
 �������ǰ�벿����ת�����벿�ֽ��бȽϣ�����ͬ��Ϊ�������������ǡ�