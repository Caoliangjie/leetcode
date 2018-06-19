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
* # �ܽ����
��һ������ĳ��ȴ�����һ����������������ĳ��ȣ�Ȼ������Ƚϣ��ҵ���ͬ�Ľڵ㡣