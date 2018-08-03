* # �������
A robot is located at the top-left corner of a m x n grid (marked 'Start' in the diagram below).

The robot can only move either down or right at any point in time. The robot is trying to reach the bottom-right corner of the grid (marked 'Finish' in the diagram below).

How many possible unique paths are there?
һ��������λ��һ�� m x n ��������Ͻ� ����ʼ������ͼ�б��Ϊ��Start�� ����

������ÿ��ֻ�����»��������ƶ�һ������������ͼ�ﵽ��������½ǣ�����ͼ�б��Ϊ��Finish������

���ܹ��ж�������ͬ��·����

* # ���ʵ��
```c
class Solution {
public:
    int uniquePaths(int m, int n) {
        int arr[m][n];  
        arr[0][0] = 0;  
        for(int i = 0;i<m;i++)  
            arr[i][0] = 1;  
        for(int j = 0;j<n;j++)  
            arr[0][j] = 1;  
        for (int i = 1; i < m; ++i) {
            for (int j = 1; j < n; ++j) {
                arr[i][j] = arr[i - 1][j] + arr[i][j - 1];
            }
        }
        return arr[m-1][n-1];
    }
};
```
```python
class Solution:
    def uniquePaths(self, m, n):
        """
        :type m: int
        :type n: int
        :rtype: int
        """
        import numpy
        dp = [[0]*n for i in range(m)]
        for i in range(m):
            dp[i][0] = 1
        for i in range(n):
            dp[0][i] = 1      
        for i in range(1,m):
            for j in range(1,n):
                dp[i][j] = dp[i-1][j]+dp[i][j-1]
        
        return dp[m-1][n-1]
```

* # �ܽ����
  ����i��j��λ��ֻ�ܴ������������ߵ������������¹�ϵarr[i][j] = arr[i - 1][j] + arr[i][j - 1];
