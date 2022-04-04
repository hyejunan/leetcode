### 1480. Running Sum of 1d Array

***Easy***

Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).

Return the running sum of nums.

```Java
class Solution {
    public int[] runningSum(int[] nums) {
        int len = nums.length;
        int sum = 0;
        for(int i=0;i<len;i++) {
            sum += nums[i];
            if(i != 0)
                nums[i] = sum;
        }
        return nums;
    }
}
```
