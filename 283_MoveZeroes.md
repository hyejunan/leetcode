### 283. Move Zeroes

***Easy***

Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Note that you must do this in-place without making a copy of the array.

```Java
class Solution {
    public void moveZeroes(int[] nums) {
        int idx = 0;
        for(int i=0;i<nums.length;i++) {
                if(nums[i]!=0) {
                    nums[idx++] = nums[i];
                }
        }
        for(;idx<nums.length;idx++) {
            nums[idx] = 0;
        }
    }
}
```
Runtime: 1 ms, faster than 100.00% of Java online submissions for Move Zeroes.
Memory Usage: 43.7 MB, less than 85.12% of Java online submissions for Move Zeroes.
