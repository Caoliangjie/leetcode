* # �������
�����������飬дһ���������������ǵĽ�����

����:
���� nums1 = [1, 2, 2, 1], nums2 = [2, 2], ���� [2, 2]. </br>
Given two arrays, write a function to compute their intersection.

Example:
Given nums1 = [1, 2, 2, 1], nums2 = [2, 2], return [2, 2].
* # ���ʵ��
```c
class Solution {
public:
    vector<int> intersect(vector<int>& nums1, vector<int>& nums2) {
       unordered_map<int,int> m;
       vector<int> insectArray;
       int i,j;
       for (i=0;i<nums1.size();i++)
           m[nums1[i]]++;
       for (j=0;j<nums2.size();j++) {
           if (m[nums2[j]]>0) {
               
               insectArray.push_back(nums2[j]); 
               m[nums2[j]]--;
           }
       }
       return insectArray;
    }
};
```
* # �ܽ����
  1����һ��hash���� m���ȱ���nums1���ظ��ĸ�����
  2���ڶ���ѭ���У�����nums2���飬���ظ���Ԫ����ӵ�insecArray��.