* # �������
����һ�����飬���ĵ� i ��Ԫ����һ֧������Ʊ�� i ��ļ۸�

��������ֻ�������һ�ʽ��ף������������һ֧��Ʊ�������һ���㷨�����������ܻ�ȡ���������

ע���㲻���������Ʊǰ������Ʊ��
* # ���ʵ��
```c
class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int maxProfit = 0;  
        for(int i = 1; i < prices.size(); i++)
        { 
              
             maxProfit += max(0,prices[i]-prices[i-1]);
        }  
        return maxProfit;  
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
        maxProfit = 0
        for i in range(1,len(prices)):
            
            maxProfit += max(0,prices[i]-prices[i-1])
        
        return maxProfit
                        
```
* # �ܽ����
  ÿ��prices[i]-prices[i-1]>0������������Ӹ�maxProfit��
