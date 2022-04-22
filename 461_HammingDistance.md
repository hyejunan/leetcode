### 461. Hamming Distance

***Easy***

Given a fixed-length integer array arr, duplicate each occurrence of zero, shifting the remaining elements to the right.

Note that elements beyond the length of the original array are not written. 
Do the above modifications to the input array in place and do not return anything.

```Java
class Solution {
    public int hammingDistance(int x, int y) {
        return Integer.bitCount(x ^ y);
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Hamming Distance.
Memory Usage: 42 MB, less than 6.90% of Java online submissions for Hamming Distance.
