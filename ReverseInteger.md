### 7. Reverse Integer

***Medium***

Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

Assume the environment does not allow you to store 64-bit integers (signed or unsigned).

```C++
class Solution {
public:
    int reverse(int x) {
        int negFlag = 1, cnt = 0;
        unsigned int revers = 0;
        unsigned int temp, y;
        if(x < 0) {
            negFlag = -1;
        }
        if(x == -2147483648) 
            y= 2147483648;
        else
            y = negFlag*x;
        temp = y;
        while(temp != 0) {
            temp = temp / 10;
            cnt++;
        }
        temp = y;
        if (cnt == 10 && temp % 10 > 2)
            return 0;
        while(cnt!=0) {
            --cnt;
            revers = revers+(temp % 10)*pow(10,cnt);
            temp = temp / 10;
        }
        if (revers > pow(2,31)-1 || (revers > pow(2,31) && negFlag==-1))
            revers = 0;
        return negFlag*(int)revers;
    }
};
````
```JavaScript
/**
 * @param {number} x
 * @return {number}
 */
var reverse = function(x) {
    var flag = 1;
    if(x < 0) {
        flag = -1;
        x = flag*x;
    }
    var res = x.toString().split('').reverse().join('');
    var output = Number(res);
    if (flag*output <= -2147483648 || flag*output >= 2147483647)
        return 0;
    else
        return flag*output;
};
````
```Java
class Solution {
    public int reverse(int x) {
        long res = 0;
        while(x!=0) {
            res = res*10 + x%10;
            x = x/10;
        }
        if(res <= Integer.MIN_VALUE || res >= Integer.MAX_VALUE)
            return 0;
        else
            return (int)res;
    }
}
```
