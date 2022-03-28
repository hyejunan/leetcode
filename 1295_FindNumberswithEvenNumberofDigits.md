### 1295. Find Numbers with Even Number of Digits

***Easy***

Given an array nums of integers, return how many of them contain an even number of digits.

```Java
class Solution {
    public void duplicateZeros(int[] arr) {
        int len = arr.length;
        int[] temp = new int[len];
        for(int i=0;i<len;i++) {
            temp[i] = arr[i];
        }
        int j = 0;
        for(int i=0;i<len;i++) {
            if(temp[j] == 0 && i+1 < len) {
                arr[i] = 0;
                arr[i+1] =0;
                i++;
            }
            else 
                arr[i] = temp[j];
            j++;
        }

    }
}
```
