### 1389. Create Target Array in the Given Order

***Easy***

Given two arrays of integers nums and index. Your task is to create target array under the following rules:

Initially target array is empty.
From left to right read nums[i] and index[i], insert at index index[i] the value nums[i] in target array.
Repeat the previous step until there are no elements to read in nums and index.
Return the target array.

It is guaranteed that the insertion operations will be valid.

```Java
class Solution {
    public int[] createTargetArray(int[] nums, int[] index) {
        ArrayList<Integer> arrlist = new ArrayList<Integer>();
        int[] target = new int[nums.length];
        
        for(int i=0;i<nums.length;i++) {
            arrlist.add(index[i], nums[i]);
        }
        for(int i=0;i<nums.length;i++) {
            target[i] = arrlist.get(i);
        }
        return target;
    }
}
```
Runtime: 0 ms
Memory Usage: 40.8 MB
