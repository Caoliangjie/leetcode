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
* # �ܽ����
 һ��ʼֱ���õݹ�ķ��������ǳ�ʱ�ˣ�ԭ�����ظ����˺ܶ�飬������һ�����鱣���м�ֵ�������Ϳ��Լ�����������