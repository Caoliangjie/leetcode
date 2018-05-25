* # �������
You are given an n x n 2D matrix representing an image.

Rotate the image by 90 degrees (clockwise).

Note:

You have to rotate the image in-place, which means you have to modify the input 2D matrix directly. DO NOT allocate another 2D matrix and do the rotation.
����һ�� n �� n �Ķ�ά�����ʾһ��ͼ��

��ͼ��˳ʱ����ת 90 �ȡ�
* # ���ʵ��
```c
class Solution {
public:
    void rotate(vector<vector<int>>& matrix) {
         int len = matrix.size();
        for (int i = 0; i < len; i++) {
         for (int j = 0; j < len - i; j++) {
             int tmp = matrix[i][j];
             matrix[i][j] = matrix[len - j - 1][len - i - 1];
             matrix[len - j - 1][len - i - 1] = tmp;
         }
     }

    
     for (int i = 0; i < len; i++) {
         for (int j = 0; j < len / 2; j++) {
             int tmp = matrix[j][i];
             matrix[j][i] = matrix[len - j - 1][i];
             matrix[len - j - 1][i] = tmp;
         }
     }
         
    }
};
```
* # �ܽ����
   ���ȹ۲�������û��ʲô��ת���ɣ�����۲첻���������£������Ƚ����Խ�Ԫ�أ�Ȼ���ٽ�����Ԫ�ء�