* # �������
Given an array of strings, group anagrams together.

����һ���ַ������飬����ĸ��λ�������һ����ĸ��λ��ָ��ĸ��ͬ�������в�ͬ���ַ�����
* # ���ʵ��
```c
class Solution {
public:
    vector<vector<string>> groupAnagrams(vector<string>& strs) {
         vector<vector<string>> vec;
         unordered_map<string, vector<string>> m;
          for (auto str : strs) {
              string t = str;
              sort(t.begin(), t.end());
             m[t].push_back(str);
        }
         for (auto m1 : m) {
             vec.push_back(m1.second);
         }
        return vec;
    }
    
};
```
* # �ܽ����
����ĸ��λ���������к󣬻�õ���ͬ�Ľ�������Խ���һ��ӳ�����ÿ���ַ��������������ַ�����Ϊkey��Ȼ���ٰ�key��Ӧ��value�����ά����vec�С�