### 977. Squares of a Sorted Array

***Easy***

Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.

```Java
class Solution {
    public int[] sortedSquares(int[] nums) {
        int len = nums.length;
        int[] temp = new int[len];
        for(int i=0;i<len;i++) {
            temp[i] = nums[i] * nums[i];
        }
        Arrays.sort(temp);
        return temp;
    }
}
```
