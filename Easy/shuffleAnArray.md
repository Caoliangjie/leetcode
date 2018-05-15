* # �������
����һ��û���ظ�Ԫ�ص�����
// �����ּ��� 1, 2 �� 3 ��ʼ�����顣
int[] nums = {1,2,3};
Solution solution = new Solution(nums);

// �������� [1,2,3] �����ؽ�����κ� [1,2,3]�����з��صĸ���Ӧ����ͬ��
solution.shuffle();

// �������鵽���ĳ�ʼ״̬[1,2,3]��
solution.reset();

// �����������[1,2,3]���Һ�Ľ����
solution.shuffle();
* # ���ʵ��
```c
class Solution {
       vector<int> v;  
public:
    Solution(vector<int> nums): v(nums) {
        
    }
    
   
   /** Resets the array to its original configuration and return it. */
    vector<int> reset() {
         return v;  
    }
    
    /** Returns a random shuffling of the array. */
    vector<int> shuffle() {
        vector<int> data = v;
        for(int i=data.size()-1; i>=0; i--)  
            swap(data[i], data[rand()%(i+1)]);  
        return data;  
    }    
    
};
```
* # �ܽ����
����������һ��Ԫ�ؿ�ʼ��ѡȡȡ��������һԪ�غ�����������ѡ��ѡ����λ�ã��������ƣ�ֱ������ȫ�����ҡ�