* # �������
Given an unsorted array of integers, find the length of longest increasing subsequence.
����һ��������������飬�ҵ���������������еĳ��ȡ�

* # ���ʵ��
```c
class Solution {
public:
    int lengthOfLIS(vector<int>& nums) {
            
    vector<int> vec(nums.size());
    
    int sum=0;  
    for(int i=0;i<nums.size();i++){  
        vec[i]=1;
        for(int j=0;j<i;j++){  
            if(nums[i]>nums[j])  
            vec[i]=max(vec[i],vec[j]+1);  
        } 
        
        sum=max(sum,vec[i]);  
    }  
        
    return sum; 
    }
};
```

* # �ܽ����
vec[i]��ʾ�Ե���i�����ֵ�����������еĳ��ȣ�ֻ���������֮ǰ�����֣��������֮ǰ�����ִ���ôѡ���������֮������������г���+1�����й�ϵʽvec[i]=max(vec[i],vec[j]+1)��