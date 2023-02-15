***Question***:-


**Pow(x,n)**


Implement pow(x, n), which calculates x raised to the power n (i.e., xn).


Example 1:
```
Input: x = 2.00000, n = 10
Output: 1024.00000
```
Example 2:
```
Input: x = 2.10000, n = 3
Output: 9.26100
```
Example 3:
```
Input: x = 2.00000, n = -2
Output: 0.25000
Explanation: 2-2 = 1/22 = 1/4 = 0.25
```

**Solution**
```
#include<bits/stdc++.h>
using namespace std;

class Solution{
    public:
    double myPow(double x, int n){
        if(n==0 || x ==1){
            return 1;
        }
        double pow=myPow(x,n/2);
        pow*=pow;

        if(n%2==0){
            return pow;
        }
        else{
            if(n<n){
                return pow*(1/x);
            }
            return pow*x;
        }
    }
};
int main(){
    Solution sb;
    double x = 2.00000;
    int n = 10;
    cout<<sb.myPow(x,n);
    return 0;
}
```

**This Program Output is**:--
```
1024
```
