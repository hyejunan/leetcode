### 1929. Concatenation of Array

***Easy***

Given an integer array nums of length n, you want to create an array ans of length 2n where ans[i] == nums[i] and ans[i + n] == nums[i] for 0 <= i < n (0-indexed).

Specifically, ans is the concatenation of two nums arrays.

Return the array ans.

```Java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int len = nums.length;
        int[] res = new int[len*2];
        
        for(int i=0;i<len*2;i++) {
            res[i] = nums[i%len];
        }
        return res;
    }
}
```
