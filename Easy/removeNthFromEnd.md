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
class Solution:
    def removeNthFromEnd(self, head, n):
        """
        :type head: ListNode
        :type n: int
        :rtype: ListNode
        """
        if not head.next :
            return None
        q, p = head, head
        num = 0
        tmp = 0
        while p is not None:
            p = p.next
            num += 1
        if n == num:
            return head.next
        m = num - n -1
        while m > tmp:
            q = q.next
            tmp +=1
            
        q.next = q.next.next
        return head
```
* # �ܽ����
  ͳ�������ȣ��ҵ���ɾ���Ǹ����ǰ����㣬����ɾ��,ע�⵱�����Ⱥ�n��ȵ������
