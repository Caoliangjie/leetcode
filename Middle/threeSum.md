* # �������
Given an array nums of n integers, are there elements a, b, c in nums such that a + b + c = 0? Find all unique triplets in the array which gives the sum of zero.
����һ������ n ������������ nums���ж� nums ���Ƿ��������Ԫ�� a��b��c ��ʹ�� a + b + c = 0 ���ҳ��������������Ҳ��ظ�����Ԫ�顣
* # ���ʵ��
```c
class Solution {
public:
    vector<vector<int>> threeSum(vector<int>& nums) {
        vector<int> numSet(3);
        vector<vector<int>> vec;
        sort(nums.begin(), nums.end());
        int sum;
        int len = nums.size();
        for(int i = 0; i < len-2; i++) {
            sum = 0 - nums[i];
            numSet[0] = nums[i];
            for(int j = i+1, k = len-1; j < k;) {
                if(nums[j] + nums[k] == sum) {
                    numSet[1] = nums[j++];
                    numSet[2] = nums[k--];
                    vec.push_back(numSet);

                    while(j < k && nums[j] == nums[j-1]) 
                        j++;
                    while(j < k && nums[k] == nums[k+1])
                        k--;
                }
                else if(nums[j] + nums[k] < sum)
                    j++;
                else 
                    k--;
            }
            while(i < len-2 && nums[i+1] == nums[i])
                i++;
        }
        return vec;
    }
};
```

* # �ܽ����
 ��������ת��Ϊ���������⡣�Ƚ�����������������ָ��p,q,r��pָ��ָ���һ����x��q,rָ��������ʣ�����е�������q��r��ָ���������Ϊ-x����pָ���һ���������������Ϻ󣬽�p���ơ�һֱ������pָ�������е�������������������������������ظ��������