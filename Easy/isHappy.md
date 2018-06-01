* # �������

Write an algorithm to determine if a number is "happy".

A happy number is a number defined by the following process: Starting with any positive integer, replace the number by the sum of the squares of its digits, and repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle which does not include 1. Those numbers for which this process ends in 1 are happy numbers.

��дһ���㷨���ж�һ�����ǲ��ǡ�����������

һ����������������Ϊ������һ����������ÿһ�ν������滻Ϊ��ÿ��λ���ϵ����ֵ�ƽ���ͣ�Ȼ���ظ��������ֱ���������Ϊ 1��Ҳ����������ѭ����ʼ�ձ䲻�� 1��������Ա�Ϊ 1����ô��������ǿ�������
* # ���ʵ��
```c
class Solution {
public:
bool isHappy(int n) {  
         
        set<int> s;  
        while(1) {  
            if(n == 1) return true;  
            if(s.count(n) == 1) return false;  
            s.insert(n);  
            n = happyNumber(n);  
        }  
    }  
      
    int happyNumber(int n) {  
        int sum = 0;  
        while(n!= 0) {  
            sum += (n%10)*(n%10);  
            n /= 10;  
        }  
        
        return sum;  
    }  
};
```
* # �ܽ����
 ��һ��set�������жϳ��ֵ���֮ǰ�Ƿ���ֹ���������ֹ����������ѭ���������ǿ�������