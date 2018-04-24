 * # �������
 Implement atoi which converts a string to an integer.

The function first discards as many whitespace characters as necessary until the first non-whitespace character is found. Then, starting from this character, takes an optional initial plus or minus sign followed by as many numerical digits as possible, and interprets them as a numerical value.

The string can contain additional characters after those that form the integral number, which are ignored and have no effect on the behavior of this function.

If the first sequence of non-whitespace characters in str is not a valid integral number, or if no such sequence exists because either str is empty or it contains only whitespace characters, no conversion is performed.

If no valid conversion could be performed, a zero value is returned.
ʵ�� atoi�����ַ���תΪ������

���ҵ���һ���ǿ��ַ�֮ǰ����Ҫ�Ƴ����ַ����еĿո��ַ��������һ���ǿ��ַ������Ż򸺺ţ�ѡȡ�÷��ţ�����������澡���ܶ����������������������ⲿ���ַ���Ϊ������ֵ�������һ���ǿ��ַ������֣���ֱ�ӽ�����֮�������������ַ�����������γ�������

�ַ����������γ��������ַ��������������ַ�����Щ�ַ����Ա����ԣ����Ƕ��ں���û��Ӱ�졣

���ַ����еĵ�һ���ǿ��ַ����в��Ǹ���Ч�����������ַ���Ϊ�գ����ַ����������հ��ַ�ʱ���򲻽���ת����

����������ִ����Ч��ת�������� 0��
* # ���ʵ��
```c
class Solution {
public:
    int myAtoi(string str) {
             int i=0,sign=1,num = 0;  
     if(str.size()==0)  
         return 0;  
     while(str[i]==' '&& i<str.size()){  
         i++;  
     }  
     if(str[i]=='+'||str[i]=='-'){  
         sign = str[i]=='+'?1:-1;  
         i++;  
     }  
     while(i<str.size()){  
         int digit= str[i]-'0';  
         if (digit<0||digit>9){  
             break;  
         }  
         if(INT_MAX/10 < num || INT_MAX/10 == num && INT_MAX %10 < digit){  
             return sign == 1 ? INT_MAX : INT_MIN;  
         }  
         num = 10 * num + digit;  
            i ++;  
     }
        return num*sign;
    }
};
```
* # �ܽ����
 �����ѵ�������Ҫ���Ǹ���������������������е�Ҳ�г�����࿼�ǲ���֮����
};