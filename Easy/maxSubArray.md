* # �������
����һ���������� nums ���ҵ�һ���������͵����������飨���������ٰ���һ��Ԫ�أ������������͡�
* # ���ʵ��
```c
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
         int n = nums.size();  
        int max = nums[0];
        int sum = 0;
        for(int i=0;i<n;i++)
        {
            sum += nums[i];
            if(sum > max)  
            {  
                max = sum;  
            }  
            if(sum < 0)  
            {  
                sum = 0; 
            }  
        }  
        return max;  
    }
};
```
```python
class Solution:
    def maxSubArray(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        maxSum = []
        maxSum.append(nums[0])
        
        for i  in range(1,len(nums)):
            maxSum.append(max(nums[i],maxSum[i-1]+nums[i]))
        
        return max(maxSum)
```
* # �ܽ����
  ���ִ���Ϊ�������ִ��������������Դ����ټ�������ʹʱ�临�ӶȴﵽO(n)��
�ö�̬�滮��˼�룬maxSum[i]=max(nums[i],nums[i]+max[i-1]),maxSum[i]��ʾΪ����i��Ԫ�ص��������͡�
