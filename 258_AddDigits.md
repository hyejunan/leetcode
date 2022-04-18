### 258. Add Digits

***Easy***

Given an integer num, repeatedly add all its digits until the result has only one digit, and return it.

```Java
class Solution {
    public int addDigits(int num) {
        int sum = 0;
        while(num > 0) {
            sum = sum + num % 10;
            num = num / 10; 
        }
        if(sum >= 10) {
            sum = addDigits(sum);
        }
        return sum;
    }
}
```
Runtime: 1 ms, faster than 96.29% of Java online submissions for Add Digits.
Memory Usage: 39.1 MB, less than 98.54% of Java online submissions for Add Digits.
