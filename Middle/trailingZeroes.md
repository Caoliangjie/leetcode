* # �������
Given an integer n, return the number of trailing zeroes in n!.

����һ������ n������ n! ���β�������������
* # ���ʵ��

```c
class Solution {
public:
    int trailingZeroes(int n) {
        int sum = 0;
            while(n){
                sum += n/5;
                n /=5;
            }
        return sum;
    }
};
```

* # �ܽ����
Ҫ��ý׳˺�0�ø�������ʵҲ����Ҫ�ҳ�����10�ĸ��������԰�10�ֽ�Ϊ2��5������֪��2�ı��������϶��Ƕ���5�ı������������Դ������Ҫ���5�ĸ�����������25,125������������ֻ����һ��5��