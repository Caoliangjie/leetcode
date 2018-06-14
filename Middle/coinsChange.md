* # �������
You are given coins of different denominations and a total amount of money amount. Write a function to compute the fewest number of coins that you need to make up that amount. If that amount of money cannot be made up by any combination of the coins, return -1.

������ͬ����Ӳ�� coins ��һ���ܽ�� amount����дһ��������������Դճ��ܽ����������ٵ�Ӳ�Ҹ��������û���κ�һ��Ӳ�����������ܽ����� -1��



* # ���ʵ��
```c
class Solution {
public:
    int coinChange(vector<int>& coins, int amount) {
        vector<int> dp(amount+1, 100);
        dp[0] = 0;
        for(int i = 0; i < coins.size(); i++){
            for(int j = 0; j <= amount - coins[i]; j++){
                dp[j+coins[i]] = min(dp[j+coins[i]], dp[j]+1);
            }
        }
        if(dp[amount] == 100)
            return -1;
        return dp[amount];
    }
};
```

* # �ܽ����
 �ö�̬�滮����dp[j] Ϊ�һ�amount���ٵ�Ӳ������

���У�dp[j + coins[i] ] = min(dp[j + coins[i] ] , dp[j] + 1��

