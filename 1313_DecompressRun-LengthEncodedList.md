### 1313. Decompress Run-Length Encoded List

***Easy***

We are given a list nums of integers representing a list compressed with run-length encoding.

Consider each adjacent pair of elements [freq, val] = [nums[2*i], nums[2*i+1]] (with i >= 0).  
For each such pair, there are freq elements with value val concatenated in a sublist. 
Concatenate all the sublists from left to right to generate the decompressed list.

Return the decompressed list.

```Java
class Solution {
    public int[] decompressRLElist(int[] nums) {
        int freq=0, val;
        int[] freqArray = new int[nums.length/2];
        int[] valArray = new int[nums.length/2];
        for(int i=0;i<nums.length/2;i++) {
            freq = freq + nums[2*i];
            freqArray[i] = nums[2*i];
            valArray[i] = nums[2*i+1];
        }
        int[] digits = new int[freq];
        int idx = 0;
        for(int i=0;i<valArray.length;i++) {
            for(int j=0;j<freqArray[i];j++) {
                digits[idx++] = valArray[i]; 
            }
        }
        return digits;
    }
}
```
53 / 53 test cases passed.
Status: Accepted
Runtime: 4 ms
Memory Usage: 44.8 MB
