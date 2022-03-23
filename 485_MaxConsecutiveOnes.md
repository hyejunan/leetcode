### 485. Max Consecutive Ones

***Easy***

Given a binary array nums, return the maximum number of consecutive 1's in the array.

```Java
class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
        int res = 0;
        int temp = 0;
        for(int i:nums) {
            if(i == 1) {
                res++;
                if(res > temp)
                    temp = res;
            }
            else 
                res = 0;;

        }
        return temp;
    }
}
```
