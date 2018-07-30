* # �������
����һ�����飬���ĵ� i ��Ԫ����һ֧������Ʊ�� i ��ļ۸�

���һ���㷨�����������ܻ�ȡ�������������Ծ����ܵ���ɸ���Ľ��ף��������һ֧��Ʊ����

ע�⣺�㲻��ͬʱ�����ʽ��ף���������ٴι���ǰ���۵�֮ǰ�Ĺ�Ʊ����
Say you have an array for which the ith element is the price of a given stock on day i.

Design an algorithm to find the maximum profit. You may complete as many transactions as you like (i.e., buy one and sell one share of the stock multiple times).
* # ���ʵ��
```c
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int max_profit = 0;
        if(prices.size() == 0)
            return 0;
        int min_buy = prices[0];        
        for(int i = 1;i< prices.size() ;i++){
            max_profit = max(max_profit,prices[i] - min_buy);
            min_buy = min(min_buy,prices[i]);
        }
        return max_profit;
    }
};
```
```python
class Solution:
    def maxProfit(self, prices):
        """
        :type prices: List[int]
        :rtype: int
        """
        if len(prices)==0: return 0
        max_profit = 0
        min_buy = prices[0]
        for i in range(1,len(prices)):
            max_profit = max(max_profit,prices[i]-min_buy)
            min_buy = min(min_buy,prices[i])
        
        return max_profit
```
* # �ܽ����
���ڲ��޹������������ֻҪ��׬Ǯ�����������ɣ�Ȼ��ͳ������
