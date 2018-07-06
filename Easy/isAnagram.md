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
        vector<int> v1(26);
        vector<int> v2(26);
        if(s.size()!=t.size())
            return false;
        for(int i=0;i<s.size();i++)
        {
            m1[s[i]-'a']++;
            m2[t[i]-'a']++;
        }
        for(int i=0;i<26;i++)
        {
            if(m1[i]!=m2[i])
                return false;
        }
        
        return true;
    }
};
```
```c
class Solution {
public:
    bool isAnagram(string s, string t) {
       vector<int> vec(26);
      for(auto c:s){
        vec[c-'a']++;
     }
     for(auto c:t){
         vec[c-'a']--;
     }
     for(int i=0;i<26;i++){
         if(vec[i]!=0)
             return false;
     }
        
        return true;
    }
};
```
* # �ܽ����
 ������ӳ����ֱ�ͳ��ÿ���ַ����У�ÿ����ĸ�ĸ������������ַ�����ÿ����ĸ������ͬ���򷵻�false��
���򷵻�true��
�ڶ��ַ�������ͳ�Ƶ�һ���ַ���ÿ����ĸ�ĸ�����Ȼ������ڶ����ַ�����ÿ����ĸ�ĸ�����һ��ȥ�������Ϊ0���򷵻�false��