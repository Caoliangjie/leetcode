* # �������
Given an array of integers, every element appears twice except for one. Find that single one.
Note:
Your algorithm should have a linear runtime complexity. Could you implement it without using extra memory?

���� �� ����һ���������飬����һ��Ԫ���⣬ÿ��Ԫ�ض���������Ρ��ҵ���һ����           

ע��   ����㷨Ӧ����һ����������ʱ�����ԡ�����Բ�ʹ�ö�����ڴ���ʵ������

* # ���ʵ��
```c
class Solution {
public:
    int singleNumber(vector<int>& nums) {
        int  sign=0;
        for(int i=0;i<nums.size();i++)
        {
            sign ^= nums[i];
        }
        
        return sign;
    }
};
```
* # �ܽ����
 ��ʵ����һ��Ӧ���ÿռ任ʱ�䣬�ù�ϣ���㣬����Ŀ������Ҫ�󣬲��ö�����ڴ棬
 ��Ϊ0���κ����������ȥ�䱾���������������ķ�ʽ����⡣
};