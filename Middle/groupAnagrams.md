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
```python
class Solution:
    def groupAnagrams(self, strs):
        """
        :type strs: List[str]
        :rtype: List[List[str]]
        """      
        li = {}
        for st in strs:
            st_sorted = "".join(sorted(st))
            if st_sorted in li :
                li[st_sorted].append(st)
            else:
                li[st_sorted] = [st]
               
        return list(li.values())
```
* # �ܽ����
����ĸ��λ���������к󣬻�õ���ͬ�Ľ�������Խ���һ��ӳ�����ÿ���ַ��������������ַ�����Ϊkey��Ȼ���ٰ�key��Ӧ��value�����ά����vec�С�
�ù�ϣ��洢��˼�룬���������ַ�����Ϊ������ѯ�ֵ����Ƿ�������ַ�����������ӣ�û��������
