### 1528. Shuffle String

***Easy***

You are given a string s and an integer array indices of the same length. The string s will be shuffled such that the character at the ith position moves to indices[i] in the shuffled string.

Return the shuffled string.

```Java
class Solution {
    public String restoreString(String s, int[] indices) {
        char[] res = new char[indices.length];
        for(int i=0;i<indices.length;i++) {
            res[indices[i]] = s.charAt(i);
        }
        return new String(res);
    }
}
```
Runtime: 1 ms, faster than 91.01% of Java online submissions for Shuffle String.
Memory Usage: 42.7 MB, less than 81.21% of Java online submissions for Shuffle String.
