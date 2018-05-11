* # �������
����һ���Ǹ����� numRows������������ǵ�ǰ numRows �С�

* # ���ʵ��
```c
class Solution {
public:
    vector<vector<int>> generate(int numRows) {
        
        vector<int> column;
        vector<vector<int>> arr(numRows,column);       
        for(int i = 0;i < numRows;i++)
        {
            arr[i].push_back(1);            
            for(int j = 1;j <= i-1;j++)
            {
                arr[i].push_back(arr[i-1][j]+arr[i-1][j-1]);
            }
            if(i > 0)
            {
                arr[i].push_back(1);
            }
            
        }      
        return arr;
        
    }  
};
```
* # �ܽ����
  ��������arr[i-1][j]+arr[i-1][j-1]����һ�е�Ԫ�س�����β֮�⣬���ǽ���һ�����ڵ���Ԫ����ӡ�