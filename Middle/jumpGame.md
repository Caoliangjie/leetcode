* # �������

Given an array of non-negative integers, you are initially positioned at the first index of the array.

Each element in the array represents your maximum jump length at that position.

Determine if you are able to reach the last index.
����һ���Ǹ��������飬�����λ������ĵ�һ��λ�á�

�����е�ÿ��Ԫ�ش������ڸ�λ�ÿ�����Ծ����󳤶ȡ�

�ж����Ƿ��ܹ��������һ��λ�á�

* # ���ʵ��
```c
class Solution {
public:
    bool canJump(vector<int>& nums) {
        int loc=0;
        int i=0;
        
        for(int i=0;i<nums.size() && i<=loc;i++){
            loc=max(loc,i+nums[i]);
        }
        return loc>=nums.size()-1;
    }
};
```
* # �ܽ����
 �ж��ܷ������յ㣬�ڱ�������Ĺ����У�����ÿ������������Զ�ķ�Χ�������������Χ���ڵ����յ㣬��ô����������
