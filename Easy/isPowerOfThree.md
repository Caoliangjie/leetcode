* # �������
����һ��������дһ��������ȷ��������ǲ���3��һ����
* # ���ʵ��
```c
method 1:
class Solution {
public:
    bool isPowerOfThree(int n) {
     while(n&&n%3==0)
        {
            n/=3;
        }
        if(n==1)
            return true;
        else 
            return false;
    }
};
method 2
class Solution {
public:
    bool isPowerOfThree(int n) {
        if(n<=0)
            return false;
        int k=log(INT_MAX)/log(3);
        int b3=pow(3,k);
        if(b3%n==0)
            return true;
        else 
            return false;
    }
};
```
* # �ܽ����
  ��һ��ѭ���ķ�ʽ����������ѭ�����ҳ�int��Χ��3����������������������Ȼ���Ա�n������