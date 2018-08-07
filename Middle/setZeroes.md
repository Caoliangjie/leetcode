* # �������
Given a m x n matrix, if an element is 0, set its entire row and column to 0. Do it in-place.

����һ�� m x n �ľ������һ��Ԫ��Ϊ 0�����������к��е�����Ԫ�ض���Ϊ 0����ʹ��ԭ���㷨��
* # ���ʵ��
```c
class Solution {
public:
    void setZeroes(vector<vector<int>>& matrix) {
        if(matrix.size() == 0) 
            return;
        bool rowZero = false, colZero = false; // ��¼��ЩԪ�ص�������Ҫ���㣬�ж����������Ƿ�Ҫ��0
        for(int i = 0; i < matrix.size(); i++){
            for(int j = 0; j < matrix[0].size(); j++){
                if(i != 0 && j != 0 && matrix[i][j] == 0){
                    matrix[i][0] = 0;
                    matrix[0][j] = 0;
                } else if (matrix[i][j] == 0){  // ����������Ϊ�㣬�����ǡ�
                    rowZero = i == 0 ? true : rowZero;
                    colZero = j == 0 ? true : colZero;
                }
            }
        }
        
        for(int i = 1; i < matrix.size(); i++){    // �����������е�Ԫ������
            for(int j = 1; j < matrix[0].size(); j++){
                if(matrix[0][j] == 0 || matrix[i][0] == 0){
                    matrix[i][j] = 0;
                }
            }
        }

        for(int i = 0; colZero && i < matrix.size(); i++){ //��������
            matrix[i][0] = 0;
        }
  
        for(int j = 0; rowZero && j < matrix[0].size(); j++){ //��������
            matrix[0][j] = 0;
        }
    }
};
```
```python
class Solution:
    def setZeroes(self, matrix):
        """
        :type matrix: List[List[int]]
        :rtype: void Do not return anything, modify matrix in-place instead.
        """
        l1 = []
        
        for i in range(len(matrix)):
            for j in range(len(matrix[i])):
                if  matrix[i][j]==0:
                    l1.append((i,j))
        
        for i,j in  l1:
            matrix[i] = [0]*len(matrix[i])
            for k in range(len(matrix)):
                matrix[k][j] = 0
        
        return 
```
* # �ܽ����
  ʹ��ԭ���㷨��⣬��¼���������е�Ԫ���⣬��ЩԪ�ص�������Ҫ��0������������bool������¼���������Ƿ�
��Ԫ��Ϊ0��������Ԫ��Ϊ0��������������ж��Ƿ���Ҫ������������0.
