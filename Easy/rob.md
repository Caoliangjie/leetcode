* # �������
You are a professional robber planning to rob houses along a street. Each house has a certain amount of money stashed, the only constraint stopping you from robbing each of them is that adjacent houses have security system connected and it will automatically contact the police if two adjacent houses were broken into on the same night.

Given a list of non-negative integers representing the amount of money of each house, determine the maximum amount of money you can rob tonight without alerting the police.
��һ��רҵ��С͵���ƻ�͵���ؽֵķ��ݡ�ÿ�䷿�ڶ�����һ�����ֽ�Ӱ����͵�Ե�Ψһ��Լ���ؾ������ڵķ���װ���໥��ͨ�ķ���ϵͳ������������ڵķ�����ͬһ���ϱ�С͵���룬ϵͳ���Զ�������

����һ������ÿ�����ݴ�Ž��ķǸ��������飬�������ڲ���������װ�õ�����£��ܹ�͵�Ե�����߽�
* # ���ʵ��
```c
class Solution {
public:
    int rob(vector<int>& nums) {
        int n = nums.size();
        if(n == 0)
            return 0;
        if(n == 1)
            return nums[0];
        int sum1,sum2; //sum1��ʾ��ٵ���i�ҵ������棬sum2��ʾ��ٵ���i-2�ҵ�������
        sum1 = sum2 = 0;
        for(int i = 0; i < n; i++){
            int tmp = sum1;
            sum1 = max(sum1, sum2+nums[i]);
            sum2 = tmp;
        }
        return sum1;
    }
};
```
* # �ܽ����
  ��sum1Ϊ��ٵ���i�ҵ������棬sum2Ϊ��ʾ��ٵ���i-2�ҵ������棬���е��ƹ�ϵsum[i]=max(sum[i-1],sum2+nums[i])������ٵ���i-1��ʱ���������ٵ���i-2�ҵ�������ϴ�ٵ�i�һ�õĽ�Ǯȡ���е����ֵ��