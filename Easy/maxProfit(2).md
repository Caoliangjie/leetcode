* # �������
����һ�����飬���ĵ� i ��Ԫ����һ֧������Ʊ�� i ��ļ۸�

��������ֻ�������һ�ʽ��ף������������һ֧��Ʊ�������һ���㷨�����������ܻ�ȡ���������

ע���㲻���������Ʊǰ������Ʊ��
* # ���ʵ��
```c
class Solution {
public:
    int maxProfit(vector<int>& prices) {
       int index;  
        int maxProfit = 0;  
        for(int i = 0; i < prices.size(); i++)
        { 
              
            for(int j=i+1;j < prices.size();j++)
            {  
                index = prices[j] - prices[i]; 
                if(index>0 && index>maxProfit)
                maxProfit = index;
                     
            }  
        }  
        return maxProfit;   
    }
};
```
* # �ܽ����
  ����ⷨ�Ƚϼ򵥣����㷨���Ӷ�ΪO��n^2��,��ʱ�Ͼá�