* # �������
����һ������ 0, 1, 2, ..., n �� n ���������У��ҳ� 0 .. n ��û�г����������е��Ǹ�����
* # ���ʵ��
```c
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int n = nums.size(),sum=0;

        
        for(int i=0;i<n;i++)
        {
            sum = sum+nums[i];
        }
         
        return n*(n+1)/2-sum;
    }
};
```
* # �ܽ����
 ����ѧ�ķ�����⼴�ɣ���0-n���ܺͼ�ȥ���������������ܺ͡�