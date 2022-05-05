### 1089. Duplicate Zeros

***Easy***

You are given an integer n and an integer start.

Define an array nums where nums[i] = start + 2 * i (0-indexed) and n == nums.length.

Return the bitwise XOR of all elements of nums.

```Java
class Solution {
    public int xorOperation(int n, int start) {
        int res = start;
        for(int i=1;i<n;i++) {
            res = res^(start+ 2 * i);       
        }
        return res;
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for XOR Operation in an Array.
Memory Usage: 41.2 MB, less than 21.54% of Java online submissions for XOR Operation in an Array.
