* # �������
���������ַ��� s �� t ����дһ���������ж� t �Ƿ��� s ��һ����ĸ��λ�ʡ�
Given two strings s and t, write a function to determine if t is an anagram of s.

For example,
s = "anagram", t = "nagaram", return true.
s = "rat", t = "car", return false.
* # ���ʵ��
```c
class Solution {
public:
    bool isAnagram(string s, string t) {
        unordered_map<int,int> m1;
        unordered_map<int,int> m2;
        if(s.size()!=t.size())
            return false;
        for(int i=0;i<s.size();i++)
        {
            m1[s[i]]++;
            m2[t[i]]++;
        }
        for(int i=90;i<130;i++)
        {
            if(m1[i]!=m2[i])
                return false;
        }
        
        return true;
    }
};
```
* # �ܽ����
 ������ӳ����ֱ�ͳ��ÿ���ַ����У�ÿ����ĸ�ĸ������������ַ�����ÿ����ĸ������ͬ���򷵻�false��
���򷵻�true��