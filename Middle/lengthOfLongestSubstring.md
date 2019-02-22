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

class Solution {
public:
    int lengthOfLongestSubstring(string s) {
        if (s.size()<=1) return s.size();
        vector<int> mark(200,-1);
        int length=0,start=0,length_max=0;
        
        for(int i=0;i<s.size();i++)
        {
            if(mark[s[i]] != -1 && mark[s[i]]>=start)
            {
                length_max = length_max > i - start? length_max: i - start;
                start = mark[s[i]] + 1;
            }
            
            mark[s[i]] = i;
        }
        
        length_max = length_max > s.length() - start? length_max: s.length() - start;
        return length_max;
    }
};
    
```
```python
class Solution:
    def lengthOfLongestSubstring(self, s):
        """
        :type s: str
        :rtype: int
        """    
        dic = {}
        max_len = 0
        sub_len = 0
        start = 0
        for i in range(len(s)):
            if s[i] in dic and dic[s[i]] >=start:

                start = dic[s[i]] +1

            sub_len = i -start +1

            dic[s[i]] = i

            max_len = max(max_len, sub_len)
        return max_len
```
* # �ܽ����
 ������forѭ����������ִ�����㣬�ڲ����ִ����յ㡣
 ��set���������Ѿ���ӵ��ִ���ÿ���ַ�����count�����ж��Ƿ��ַ��ظ����֡�
