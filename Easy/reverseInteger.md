 * # �������
  Given a 32-bit signed integer, reverse digits of an integer.
  
  ����һ�� 32 λ�з����������������е����ֽ��з�ת��

* # ���ʵ��
```c
class Solution {
public:
    int reverse(int x) {
        int reverse=0;  
        int temp;    
        int sign=1;  
        if (x<0)//���xС��0�������������  
        {  
            sign=-1;  
            x=abs(x);  
        }  
        
        while(x)
        {             
                temp=x%10;  
                reverse=reverse*10+temp;  
                x=x/10;                                 
        } 


          return reverse*sign;  
    }
};
```
* # �ܽ����
  ���ж����������Ǹ���������ת��Ϊ�������д����ڽ�������λ�����ת��