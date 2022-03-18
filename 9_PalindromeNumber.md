### 9. Palindrome Number

***Easy***

Given an integer x, return true if x is palindrome integer.

An integer is a palindrome when it reads the same backward as forward. For example, 121 is palindrome while 123 is not.

```Java
class Solution {
    public boolean isPalindrome(int x) {
        boolean res = false;
        if (x < 0)
            return false;
        else {
            int temp = x;
            long chk = 0;
            while(temp != 0) {
                chk = chk*10 + temp%10;
                temp = temp/10;
            }
            if ((int)chk == x)
                res = true;
        }
        return res;
    }
}
```
```c++
class Solution {
public:
    bool isPalindrome(int x) {
        bool res = false;
        int temp = x;
        long chk = 0;
        if(x<0)
            return res;
        while (temp!=0) {
            chk = chk*10+temp%10;
            temp = temp/10;
        }
        if(chk == x)
            res = true;
        return res;
    }
};
````
```JavaScript
/**
 * @param {number} x
 * @return {boolean}
 */
var isPalindrome = function(x) {
    var res = false
    if (x < 0)
        return res;
    var chk = x.toString().split('').reverse().join('');
    if(Number(chk) == x)
        res = true;
    return res;
};
```
