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


```c
class Solution {
public:
    vector<int> intersect(vector<int>& nums1, vector<int>& nums2) {
        int i=0,j=0;
        sort(nums1.begin(),nums1.end());
        sort(nums2.begin(),nums2.end());
        vector<int> vec;
        while(i<nums1.size() && j<nums2.size()){
            if(nums1[i]==nums2[j]){
                vec.push_back(nums1[i]);
                i++;j++;
                continue;
            }
            nums1[i]>nums2[j]?j++:i++;     
        }
        return vec;
    }
};
```
* # �ܽ����
  
1����һ��hash���� m���ȱ���nums1���ظ��ĸ�����
  2���ڶ���ѭ���У�����nums2���飬���ظ���Ԫ����ӵ�insecArray��.
��������������������ָ��Ƚ����������е�Ԫ�أ����������������У������ȣ�С���Ǹ���ǰ�ƶ���