* # �������

����һ���Ǹ�������ɵķǿ����飬�ڸ����Ļ����ϼ�һ������һ���µ����顣

���λ���ִ�����������λ�� ������ÿ��Ԫ��ֻ�洢һ�����֡�

����Լ���������� 0 ֮�⣬��������������㿪ͷ��


* # ���ʵ��
```c
class Solution {
public:
    vector<int> plusOne(vector<int>& digits) {
        int c = 1,i;
        for (int i = digits.size()- 1; i >= 0; i--) {
            if (c == 0) {
                return digits;
            }
            int tmp = digits[i] + c;
            c = tmp / 10;
            digits[i] = tmp % 10;
        }
        
        
        if (c!= 0) {
             vector<int> new1;
            for(i=0;i<digits.size();i++)
            {
                new1.push_back(0);              
            } 
            new1.insert(new1.begin(),1) ;
            return new1;
        }
        return digits;
    }
};
```
* # �ܽ����
 ����ؼ�����Խ�λ��Ĵ�����Ҫʹ���Ϊ��λ�������е�λ�����ֱ���ʹ9.
