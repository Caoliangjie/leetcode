* # �������
Given an array with n objects colored red, white or blue, sort them in-place so that objects of the same color are adjacent, with the colors in the order red, white and blue.

Here, we will use the integers 0, 1, and 2 to represent the color red, white, and blue respectively.
����һ��������ɫ����ɫ����ɫ��һ�� n ��Ԫ�ص����飬ԭ�ض����ǽ�������ʹ����ͬ��ɫ��Ԫ�����ڣ������պ�ɫ����ɫ����ɫ˳�����С�

�����У�����ʹ������ 0�� 1 �� 2 �ֱ��ʾ��ɫ����ɫ����ɫ��
* # ���ʵ��
```c
class Solution {
public:
    void sortColors(vector<int>& nums) {
        int count[3]={0};
        for(int i=0;i<nums.size();i++){
            if(nums[i]>=0 && nums[i]<=2)
                count[nums[i]]++;
        }
        
         int index = 0;
        for(int i=0;i<count[0];i++)
             nums[index++]=0;
        for(int i=0;i<count[1];i++)
             nums[index++]=1;
        for(int i=0;i<count[2];i++)
             nums[index++]=2;
    }
};
```
* # �ܽ����
 ��һ��ɨ�����飬��count�����¼ÿ����ɫ�ĸ������ڶ���ɨ�����ɫ����