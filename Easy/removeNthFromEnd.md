* # �������
����һ������ɾ������ĵ����� n ���ڵ㣬���ҷ��������ͷ��㡣
* # ���ʵ��
```c
class Solution {
public:
    ListNode* removeNthFromEnd(ListNode* head, int n) {
        ListNode* p = head;
        ListNode* q = head;
        int sum = 0;  
        int temp = 0;
        while(p != NULL)  
        {  
            sum ++;  
            p = p->next;  
        }  
        if (sum == n)  
        {  
            return head->next;  
        } 
        sum = sum - n - 1;  
        while(temp < sum)  
        {  
            temp ++;  
            head = head->next;  
        }  
        head->next = head->next->next;  
        return q; 
    }
};
```
* # �ܽ����
  ͳ�������ȣ��ҵ���ɾ���Ǹ����ǰ����㣬����ɾ��,ע�⵱�����Ⱥ�n��ȵ������
