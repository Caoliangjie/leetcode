* # �������
������������¥�ݡ���Ҫ n ������ܵ���¥����

ÿ��������� 1 �� 2 ��̨�ס����ж����ֲ�ͬ�ķ�����������¥���أ�
* # ���ʵ��
```c
class Solution {
public:
    vector<int> res;
    int  climbStairs(int n) {
    
        if (n == 0) 
        {  
            return 0;  
        }  
          
        if (n == 1) 
        {  
            return 1;  
        }  
          
        if (n == 2) 
        {  
            return 2;  
        }  
          
        if (res.size() >= (n-2)) 
        {  
            return res.at(n - 3);  
        }  
          
        res.push_back(climbStairs(n - 1) + climbStairs(n - 2));  
        return res.back();  
    }
};
```
```python
class Solution:
    def climbStairs(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n==0:
            return 0
        if n==1:
            return 1
        if n==2:
            return 2
        l1 = [0,1,2]
        
        for i in range(3,n+1):
            l1.append(l1[i-1]+l1[i-2])
        return l1.pop()
```
* # �ܽ����
 һ��ʼֱ���õݹ�ķ��������ǳ�ʱ�ˣ�ԭ�����ظ����˺ܶ�飬������һ�����鱣���м�ֵ�������Ϳ��Լ�����������
