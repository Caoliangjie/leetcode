* # �������
Write a program to find the node at which the intersection of two singly linked lists begins.
��дһ�������ҵ������������ཻ����ʼ�ڵ㡣
* # ���ʵ��
```c
class Solution {
public:
    ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {
        ListNode* p1=headA;
        ListNode* p2=headB;
        int l1=0;
        int l2=0;
        while(p1)
        {
         p1 = p1->next;
         l1++;
        }
        while(p2)
        {
         p2 = p2->next;
         l2++;
        }
        p1=headA;
        p2=headB;
        if(l1<l2){
            int n = l2 -l1 ;
            while(n)
            {
                p2 = p2->next;
                n--;
            }
        }
        else if(l1>l2){
           int n = l1 -l2 ;
            while(n)
            {
                p1 = p1->next;
                n--;
            }
        }
        while(p1!=p2){
            p1=p1->next;
            p2=p2->next;
        }
        return p1;
    }
};
```
```python
class Solution(object):
    def getIntersectionNode(self, headA, headB):
        l1,l2 = 0,0
        p1,p2 = headA,headB
        while p1:
            l1+=1
            p1 = p1.next
        while p2:
            l2+=1
            p2 = p2.next
        p1,p2 = headA,headB
        if l1 > l2:
            n = l1 - l2
            while n:
                p1 = p1.next
                n -=1
        
        elif l2 > l1:
            n = l2 - l1
            while n:
                p2 = p2.next
                n -=1
        while p1 != p2:
            p1 = p1.next
            p2 = p2.next
        
        return p1
```
* # �ܽ����
��һ������ĳ��ȴ�����һ����������������ĳ��ȣ�Ȼ������Ƚϣ��ҵ���ͬ�Ľڵ㡣
