* # �������
����һ������ɾ������ĵ����� n ���ڵ㣬���ҷ��������ͷ��㡣
* # ���ʵ��
```c
class Solution {
public:
    ListNode* removeNthFromEnd(ListNode* head, int n) {
        ListNode *p = head;  
        ListNode *p0 = head;  
        int num = 0;  
        int tmp = 0;
        while(p != NULL)  
        {  
            num += 1;  
            p = p->next;  
        }  
        if (num == n)  
        {  
            return head->next;  
        } 
        num = num - n - 1;  
        while(num != tmp)  
        {  
            tmp += 1;  
            head = head->next;  
        }  
        head->next = head->next->next;  
        return p0;  
    }
};
```
* # �ܽ����
  ͳ�������ȣ��ҵ���ɾ���Ǹ����ǰ����㣬����ɾ����