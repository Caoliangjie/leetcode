* # �������
��������֮��ĺ�������ָ�������������ֶ�Ӧ������λ��ͬ��λ�õ���Ŀ��

������������ x �� y����������֮��ĺ������롣
 * ���ʵ��
 ```c
class Solution {
public:
    int hammingDistance(int x, int y) {
        int i,l,sum=0;
        vector<int> s1;
        vector<int> s2;
        while(x||y)
        {
            s1.push_back(x%2);
            s2.push_back(y%2);
            x= x/2;
            y= y/2;
        }
        l=max(s1.size(),s2.size());
        for(i=0;i<l;i++)
        {
            if(s1[i] != s2[i])
                sum++;
        }
        
        return sum;
    }
};
```
* �ܽ����
   ����һ����������������չ�����㺺�����롣