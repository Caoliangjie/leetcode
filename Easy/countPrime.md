* # �������
ͳ������С�ڷǸ������� n ��������������
 * ���ʵ��
 ```c
class Solution {
public:
    int countPrimes(int n) {  
        int count = 0;  
        if(n > 2) 
        count ++;  
        for(int i = 3; i < n; i +=2 )
        {  
            if(isPrime(i))  
                count ++;  
        }  
        return count;  
    }
        
  
       bool isPrime(int n){  
 
    for(int i = 2; i <= sqrt(n); i ++){  
            if(n % i == 0)  
            return false;  
        }  
        return true;  
    }        
};
```
* �ܽ����
  ��kΪn��һ��Լ������n%k==0����ô��k*(n/k)==n��֪��k��n/k����һ��С�ڵ���sqrt��n��������һ�������ڣ�
  ����ֻ���ж�n�ܷ�2��3������sqrt��n�������������ж��Ƿ�Ϊ������