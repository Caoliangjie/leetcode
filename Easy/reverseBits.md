* # �������
�ߵ������� 32 λ�޷��������Ķ�����λ��

* # ���ʵ��
```c
class Solution {
public:
    uint32_t reverseBits(uint32_t n) {
        int i,l;
        vector<int> s;
        
        while (n)
        {
            s.push_back(n & 1);
            n = n>> 1;
        }
     
        int sum = 0;
        l = s.size();
        for (i = 0 ; i <l; ++i)
        {
            sum = sum + s[i] * (1 << (32 - i - 1));
        }

        return sum;
    }
};
```
* # �ܽ����
   �Ƚϼ򵥵�һ���⡣