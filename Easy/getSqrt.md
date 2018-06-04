* # �������
Implement int sqrt(int x).

Compute and return the square root of x, where x is guaranteed to be a non-negative integer.

Since the return type is an integer, the decimal digits are truncated and only the integer part of the result is returned.
ʵ�� int sqrt(int x) ������

���㲢���� x ��ƽ���������� x �ǷǸ�������

���ڷ������������������ֻ���������Ĳ��֣�С�����ֽ�����ȥ��
* # ���ʵ��
class Solution {
public:
    int mySqrt(int x) {
        if(x<=1)
            return x;
            int left = 1;
            int right = x/2;
        while(1){
            int mid = left + (right-left)/2;

            if(mid > x/mid){
                 right = mid - 1;
            }
            else{
                if(mid + 1 > x/(mid+1))
                    return mid;
                left = mid + 1;
            }
        }
    }
};

* # �ܽ����
����0��1����������ƽ����һ������1��x/2֮�䣬���Բ��ö��ַ��ķ�������������Ϊ
��mid * mid > x����right = mid -1��
���򣬵�(mid+1)*(mid+1)*>x,return mid��
�������� ��left = mid+1�� �������ֲ��ҡ�