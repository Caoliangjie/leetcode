* # �������
��дһ��������������һ���޷�������������������Ʊ��ʽ������λ��Ϊ ��1�� �ĸ�����Ҳ����Ϊ������������
* # ���ʵ��
```c
class Solution {
public:
    int hammingWeight(uint32_t n) {
        int i,l,sum=0;
        vector<int> s;
        while(n)
        {
            s.push_back(n%2);
            n= n/2;
        }
        l = s.size();
        for(l-1;l>0;l--)
        {
            if(s[l-1]==1)
                sum++;
        }
        
        return sum;
    }
};
```
* # �ܽ����
 ���޷�����������������������������������vector<int>��Ȼ��ͳ����1�ĸ�����