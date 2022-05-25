### 1588. Sum of All Odd Length Subarrays

***Easy***

Given an array of positive integers arr, calculate the sum of all possible odd-length subarrays.

A subarray is a contiguous subsequence of the array.

Return the sum of all odd-length subarrays of arr.

```Java
class Solution {
    public int sumOddLengthSubarrays(int[] A) {
        int res = 0, n = A.length;
        for (int i = 0; i < n; ++i) {
            res += ((i + 1) * (n - i) + 1) / 2 * A[i];
        }
        return res;
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Sum of All Odd Length Subarrays.
Memory Usage: 41.7 MB, less than 59.62% of Java online submissions for Sum of All Odd Length Subarrays.
