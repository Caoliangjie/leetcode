* # �������
����һ�����������һ��Ŀ��ֵ���ҳ������к�ΪĿ��ֵ����������

����Լ���ÿ������ֻ��Ӧһ�ִ𰸣���ͬ����Ԫ�ز��ܱ��ظ����á�

 Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.
* # ���ʵ��
```c
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int len = nums.size(),i,j;
        vector<int> m;
        for(i=0;i<len;i++)
        {
            for(j=i+1;j<len;j++)
            {
                if(nums[i]+nums[j]==target)
                {
                    m.push_back(i);
                    m.push_back(j);
                    return m;
                }
            }
        }
        
        return m;
    }
};  
```



```c
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int,int> m;
        for(int i=0;i<nums.size();i++)
        {
            if(m.count(target-nums[i])){

                return {i,m[target-nums[i]]};
            }
            
            m[nums[i]]=i;
        }
    }
};
```
* # �ܽ����
 
���ַ���˼·�򵥣�����forǶ��ʹ�ã�ʱ�临�Ӷ�ΪO��N^2��.
��һ��hash����Ϊ����Ԫ��ֵ��ֵΪ����Ԫ���±꣬�����ӶȽ�ΪO(n).
