* # �������
A peak element is an element that is greater than its neighbors.

Given an input array nums, where nums[i] �� nums[i+1], find a peak element and return its index.

The array may contain multiple peaks, in that case return the index to any one of the peaks is fine.
��ֵԪ����ָ��ֵ������������ֵ��Ԫ�ء�

����һ���������� nums������ nums[i] �� nums[i+1]���ҵ���ֵԪ�ز�������������

������ܰ��������ֵ������������£������κ�һ����ֵ����λ�ü��ɡ�

����Լ��� nums[-1] = nums[n] = -�ޡ�
You may imagine that nums[-1] = nums[n] = -��.
* # ���ʵ��
```c
class Solution {
public:
    int findPeakElement(vector<int>& nums) {

          
        int left = 0;  
        int right = nums.size() - 1;  
          
        while(left <= right)  
        {  
            if(left == right) return left;  
              
            int mid = left + (right - left) / 2;  
              
            if(nums[mid] < nums[mid+1])  
            {  
                left = mid + 1;  
            }  
            else  
            {  
                right = mid;  
            }  
        }  
    }
};
```

* # �ܽ����
 Ҫʵ��O(logN)���ö��ֲ��ң����nums[mid] > nums[mid+1]������mid֮ǰ���ڷ�ֵԪ�أ����nums[mid] < nums[mid+1]������mid+1֮����ڷ�ֵԪ�ء�

