 * # �������
 
 Given a 32-bit signed integer, reverse digits of an integer.
  
  
����һ�� 32 λ�з����������������е����ֽ��з�ת��


* # ���ʵ��

```c

class Solution {
public:
    int reverse(int x) {
        long long res=0;
        int sign = 1;
        if (x > 0){ 
            sign = -1; 
            x = abs(x);
        }
        while (x > 0) {
            res = res * 10 + x % 10;
            x /= 10;
        }
 
        if (res > INT_MAX) 
            res = 0;
        return res*sign;

    }
};
```

* # �ܽ����
  
���ж����������Ǹ���������ת��Ϊ�������д����ڽ�������λ�����ת��
�ϴ�û�д����������⣬�����м�����û��ͨ�������θ�����