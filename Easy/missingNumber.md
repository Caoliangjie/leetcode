* # 
�������
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

```c
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int n = nums.size();
        int result=0;
        for(int i=0;i<=n;++i)
            result^=i;
        for(int i=0;i<n;++i)
            result^=nums[i];
        return result;
    }
};
```
* # �ܽ����

 ����ѧ�ķ�����⼴�ɣ���0-n���ܺͼ�ȥ���������������ܺ͡�
�ڶ��ֽⷨ����0��n���һ�飬�ٶԸ����������һ�飬���õĽ������ȱʧ������