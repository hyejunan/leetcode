### 1920. Build Array from Permutation

***Easy***

Given a zero-based permutation nums (0-indexed), build an array ans of the same length where ans[i] = nums[nums[i]] for each 0 <= i < nums.
length and return it.

A zero-based permutation nums is an array of distinct integers from 0 to nums.length - 1 (inclusive).

```Java
class Solution {
    public int[] buildArray(int[] nums) {
        int len = nums.length;
        int[] arr = new int[len];
        
        for(int i=0;i<len;i++) {
            arr[i] = nums[nums[i]];
        }
        return arr;
    }
}
```
