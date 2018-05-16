* # �������
���һ��֧�� push��pop��top �����������ڳ���ʱ���ڼ�������СԪ�ص�ջ��

push(x) -- ��Ԫ�� x ����ջ�С�
pop() -- ɾ��ջ����Ԫ�ء�
top() -- ��ȡջ��Ԫ�ء�
getMin() -- ����ջ�е���СԪ�ء�
* # ���ʵ��
```c
class MinStack {  
public:  
    /** initialize your data structure here. */  
    MinStack() {}  
    void push(int x) {
        if (Stk.empty()) {
            Stk.push(x);
            minStk.push(x);
        }
        else {
            Stk.push(x);
            if (x <= minStk.top()) minStk.push(x);
        }
    }

    void pop() {
        if (Stk.top() == minStk.top()) {
            minStk.pop();
        }
        Stk.pop();
    }

    int top() {
        return Stk.top();
    }

    int getMin() {
        return minStk.top();
    }        
private:  
     
    stack<int>minStk;  
    stack<int>Stk; 
};  
```
* # �ܽ����
 �������ջ��һ������������Сֵ�������˵���������ջ�������⻹�ǱȽ����׵ġ���ʵ��Ҳ�����ÿ�����vector��������⡣
