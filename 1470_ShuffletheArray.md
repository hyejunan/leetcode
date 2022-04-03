### 1470. Shuffle the Array

***Easy***

Given the array nums consisting of 2n elements in the form [x1,x2,...,xn,y1,y2,...,yn].

Return the array in the form [x1,y1,x2,y2,...,xn,yn].

```Java
class Solution {
    public int[] shuffle(int[] nums, int n) {
        int len = nums.length;
        int[] res= new int[len];
        // 0 1 2 3 4 5
        // 0 3 1 4 2 5 
        int i = 0;
        int j = 0;
        while(i<len) {
            res[i] = nums[j];
            i = i + 2;
            j++;
        }
        i = 1;
        j = n;
        while(i < len){
            res[i] = nums[j];
            i = i+2;
            j++;
        }
        return res;
    }
}
```
