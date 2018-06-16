* # �������
You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

���������ǿ���������ʾ�����Ǹ�������λ����������ʽ�洢�����ǵ�ÿ���ڵ�ֻ�洢�������֡���������ӷ���һ���µ�����

����Լ���������� 0 ֮�⣬���������ֶ��������㿪ͷ��
* # ���ʵ��
```c
class Solution {
public:
    ListNode* addTwoNumbers(ListNode* l1, ListNode* l2) {
        ListNode* head = new ListNode(0);
        ListNode* cur = head;
        int c = 0;  
       while (l1 || l2 || c)   
       {  
          int sum = (l1 ? l1->val : 0) + (l2 ? l2->val : 0) + c;  
          c = sum / 10;  
          cur->next = new ListNode(sum % 10);  
          cur = cur->next;  
          l1 = l1 ? l1->next : l1;  
          l2 = l2 ? l2->next : l2;  
       }  
      
       return head->next;  
    }
};
```
* # �ܽ����
 ����������������Ӧ��λ�õ�ֵ��ӣ����ǽ�λ����Ϊ����½�һ������ڵ㡣