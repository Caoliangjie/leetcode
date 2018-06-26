* # �������
Given a string, find the length of the longest substring without repeating characters.

����һ���ַ������ҳ��������ظ��ַ�����Ӵ��ĳ��ȡ�

* # ���ʵ��
```c
class Solution {
public:
    int lengthOfLongestSubstring(string s) {
            int sum = 0;            
            set<char> setChars;
            for (int i = 0; i < s.size(); ++i) {
                for (int j = i; j < s.size(); ++j) {
                    if (setChars.count(s[j])) {
                        break;
                    } 
                    else {
                        setChars.insert(s[j]);
                    }
                }

                if (setChars.size() > sum) {
                    sum = setChars.size();
                }
                setChars.clear();
            }
       

        return sum;
      
    }
};
```

* # �ܽ����
 ������forѭ����������ִ�����㣬�ڲ����ִ����յ㡣
 ��set���������Ѿ���ӵ��ִ���ÿ���ַ�����count�����ж��Ƿ��ַ��ظ����֡�
