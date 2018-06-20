* # �������
Given a singly linked list, group all odd nodes together followed by the even nodes. Please note here we are talking about the node number and not the value in the nodes.

You should try to do it in place. The program should run in O(1) space complexity and O(nodes) time complexity.

����һ�������������е������ڵ��ż���ڵ�ֱ�����һ����ע�⣬����������ڵ��ż���ڵ�ָ���ǽڵ��ŵ���ż�ԣ������ǽڵ��ֵ����ż�ԡ�

�볢��ʹ��ԭ���㷨��ɡ�����㷨�Ŀռ临�Ӷ�ӦΪ O(1)��ʱ�临�Ӷ�ӦΪ O(nodes)��nodes Ϊ�ڵ�������
* # ���ʵ��
```c
class Solution {
public:
    ListNode* oddEvenList(ListNode* head) {
        if (!head || !head->next) return head;
        ListNode *odd = head, *even = head->next;
        while (even && even->next) {
            ListNode *tmp = odd->next;
            odd->next = even->next;
            even->next = even->next->next;
            odd->next->next = tmp;
            even = even->next;
            odd = odd->next;
        }
        return head;
    }
};
```
```c
class Solution {
public:
    ListNode* oddEvenList(ListNode* head) {
        if (!head || !head->next) return head;
        ListNode* odd=head, *even=head->next, *even_head=even;
        while(even&&even->next){
            odd->next=even->next;
            odd=odd->next;
            even->next=odd->next;
            even=even->next;
        }
        odd->next=even_head;
        return head;
    }
};
```
oddָ����ڵ㣬evenָ��ż�ڵ㣬��ż�ڵ�even����Ǹ���ڵ��ᵽodd�ĺ��棬��ǰ��ż�ڵ�ָ����һ��ż�ڵ㣬Ȼ��odd��evenǰ��һ������ʱeven��ָ��ż�ڵ㣬oddָ��ǰ��ڵ��ĩβ�����ΰ�ȫ��ż�ڵ���ǰ��

�ڶ��ַ�������һ��even_headָ�뱣��ż�ڵ�ĳ�ʼλ�ã�oddָ��evenָ�����һ����Ȼ��oddָ�����һ�����ٰ�evenָ��ָ����һ����ڵ����һ���ڵ㣬Ȼ��ż�ڵ���ƣ�������ż�������������ɡ�