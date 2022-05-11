### 1089. Duplicate Zeros

***Easy***

Given a fixed-length integer array arr, duplicate each occurrence of zero, shifting the remaining elements to the right.

Note that elements beyond the length of the original array are not written. 
Do the above modifications to the input array in place and do not return anything.

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
Runtime: 1 ms
Memory Usage: 41.9 MB
