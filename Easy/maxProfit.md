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
        int j;  
        int maxProfit = 0;  
        for(int i = 1; i < prices.size(); i++)
        { 
            j = prices[i] - prices[i - 1];  
            if(j > 0)
            {  
                maxProfit += j;  
            }  
        }  
        return maxProfit;  
    }
};
```
* # �ܽ����
���ڲ��޹������������ֻҪ��׬Ǯ�����������ɣ�Ȼ��ͳ������