* # �������
дһ����������� 1 �� n ���ֵ��ַ�����ʾ��

1. ��� n ��3�ı����������Fizz����

2. ��� n ��5�ı����������Buzz����

3.��� n ͬʱ��3��5�ı�������� ��FizzBuzz����
* # ���ʵ��
```c
class Solution {
public:
    vector<string> fizzBuzz(int n) {
        int i;
        vector<string> s;
        if(n<0)
        {
            return s;
        }
        for(int i=1;i<=n;i++)
        {
            if(i%3==0&&i%5==0)
            
                s.push_back("FizzBuzz");
            
            else if(i%3==0)
            
                s.push_back("Fizz");
            
            else if(i%5==0)
            
                s.push_back("Buzz");
            
            else          
                s.push_back(to_string(i));          
        }
        return s;
    }
};
```
* # �ܽ����
  �򵥵���ѧ���⡣