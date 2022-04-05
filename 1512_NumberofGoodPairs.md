### 1512. Number of Good Pairs

***Easy***

Given an array of integers nums, return the number of good pairs.

A pair (i, j) is called good if nums[i] == nums[j] and i < j.

```Java
class Solution {
    public int numIdenticalPairs(int[] nums) {
        int len = nums.length;
        int cnt = 0;
        for(int i = 0;i<len;i++) {
            for(int j = i+1;j<len;j++) {
                if(nums[i] == nums[j])
                    cnt++;
            }
        }
        return cnt;
    }
}
```
