* # �������
 Calculate the sum of two integers a and b, but you are not allowed to use the operator + and -.

��ʹ������� + ��-������������a ��b֮�͡�
* # ���ʵ��
```c
class Solution {
public:
    int getSum(int a, int b) {
        if(a == 0) return b ;
        if(b == 0) return a ;
        int i = a^b;
        int sum = (a&b)<<1;
        return getSum(sum,i);
    }
};
```
* # �ܽ����
 ��λ����ͨ�������Ƽӷ��ķ�ʽ��������⡣
 ���ȣ��ڶ������мӷ��У����Խ�λ��������������������㡣
 ��Σ�ֻ����1��1�������λ���������һ��λ�Ľ�λֵΪ10����10��(1&1)<<1��
 ��󣬽����������Ľ����ӣ����еݹ飬ֱ�����ٲ�����λ��