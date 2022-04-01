### 1365. How Many Numbers Are Smaller Than the Current Number

***Easy***

Given the array nums, for each nums[i] find out how many numbers in the array are smaller than it. 
That is, for each nums[i] you have to count the number of valid j's such that j != i and nums[j] < nums[i].

Return the answer in an array.

```Java
class Solution {
    public int[] smallerNumbersThanCurrent(int[] nums) {
        int len = nums.length;
        int[] res = new int[len];
        for(int i=0;i<len;i++) {
            for(int j=0;j<len;j++) {
                if(nums[i] > nums[j])
                    res[i]++;
            }
        }
        return res;
    }
}
```
