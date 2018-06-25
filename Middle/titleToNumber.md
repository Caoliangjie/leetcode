* # �������
Given a column title as appear in an Excel sheet, return its corresponding column number.

����һ��Excel����е������ƣ���������Ӧ������š�
* # ���ʵ��
```c
class Solution {
public:
    int titleToNumber(string s) {
        int l = s.size();
        int sum = 0;
        int tmp = 1;
        while(l){        
            sum = sum + (s[l-1]-'A'+1)*tmp;
            tmp = tmp * 26;
            l--;
        }
        return sum;
    }
};
```

* # �ܽ����
������������26���ƣ����к���ʮ���ƣ���26����ת��Ϊ10���ơ�