* # �������
Given an array of integers, find if the array contains any duplicates. 
Your function should return true if any value appears at least twice in the array, and it should return false if every element is distinct.

����һ���������飬�ж��Ƿ�����ظ�Ԫ�ء�

����κ�ֵ�������г����������Σ�����Ӧ�÷��� true�����ÿ��Ԫ�ض�����ͬ���򷵻� false��
* # ���ʵ��
 ```c 
class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        int  i,j;
        unordered_map<int,int>  hash;
        for(i=0;i<nums.size();i++)
            hash[nums[i]]++;
        
        for(j=0;j<nums.size();j++)
        {
            if(hash[nums[j]]>1)
                return true;
        }
        
        return false;
    }
};
```
* # �ܽ����
 ��һ��hash���飬ͳ��ÿ������Ԫ�س��ֵĴ�����������1���򷵻�true��