* # �������
Given an array of integers nums sorted in ascending order, find the starting and ending position of a given target value.

Your algorithm's runtime complexity must be in the order of O(log n).

If the target is not found in the array, return [-1, -1].


����һ�������������е��������� nums����һ��Ŀ��ֵ target���ҳ�����Ŀ��ֵ�������еĿ�ʼλ�úͽ���λ�á�

����㷨ʱ�临�Ӷȱ����� O(log n) ����

��������в�����Ŀ��ֵ������ [-1, -1]��
* # ���ʵ��
```c
class Solution {
public:
    vector<int> searchRange(vector<int>& nums, int target) {
        if(nums.empty())
            return {-1,-1};
        int first=findFirst(nums,target);
        int last=findLast(nums,target);
        return {first,last};
    }
    
    int findFirst(vector<int>& nums, int target){
        int left=0,right=nums.size()-1;
        while(left<=right){
            int mid=(left+right)/2;
            if(nums[mid]<target)
                left=mid+1;
            else
                right=mid-1;
        }
        if(left<nums.size()&&nums[left]==target)
            return left;
        return -1;
    }
    int findLast(vector<int>& nums, int target){
        int left=0,right=nums.size()-1;
        while(left<=right){
            int mid=(left+right)/2;
            if(nums[mid]<=target)
                left=mid+1;
            else
                right=mid-1;
        }
        if(right>=0&&nums[right]==target)
            return right;
        return -1;
    }
};
```
* # �ܼ���� 
���ö��ֲ��ң�Ѱ����λ�ã���������е��ֵС��target�������е�ֵ֮����������
��������е�ֵ���ڻ����target��˵��ǰ�������п�����target���������е�ֵ֮ǰ��������ң������λ�ô���ĩλ��ʱ����λ�ü�Ϊ�����е�һ�����ڻ����target��ֵ�������λ���ϵ�����target��ȣ����ظ�λ�ã����򷵻�-1��ͬ����ҵ�ĩλ�á�
����λ���ϵ�����target��ȣ��򷵻ظ�λ�ã����򷵻�-1