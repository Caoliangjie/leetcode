* # �������
Return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.<br/>
����һ�� haystack �ַ�����һ�� needle �ַ������� haystack �ַ������ҳ� needle �ַ������ֵĵ�һ��λ�� (��0��ʼ)����������ڣ��򷵻�  -1��

* # ���ʵ��
```c
class Solution {
public:
    int strStr(string haystack, string needle) {
    
        if(needle == " ") 
          return 0;  
        int l1=haystack.size();
        int l2=needle.size();
        
        if(l1 < l2) return -1;  
        
        for(int i = 0;i < l1-l2+1;i++)
        {  
            
            if(haystack.substr(i,l2) == needle)  
                return i;  
        }  
        return -1;  
    }
};
```

* # �ܽ����
  ֱ������String�е�substr�������������Կ��ٽ�����⡣