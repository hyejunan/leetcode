### 136. Single Number

***Easy***

Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.

```Java
class Solution {
    public int singleNumber(int[] nums) {
        if(nums.length == 1)
            return nums[0];
        int res = 0;
        for(int i=0;i<nums.length;i++) {
            res ^= nums[i];
        }
        return res;
    }
}
```
