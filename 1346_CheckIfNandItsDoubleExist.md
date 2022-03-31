### 1346. Check If N and Its Double Exist

***Easy***

Given an array arr of integers, check if there exists two integers N and M such that N is the double of M ( i.e. N = 2 * M).

More formally check if there exists two indices i and j such that :

i != j
0 <= i, j < arr.length
arr[i] == 2 * arr[j]

```Java
class Solution {
    public boolean checkIfExist(int[] arr) {
        for(int i=0;i<arr.length;i++) {
            if(arr[i] == 0)
                i++;
            for(int j=0;j<arr.length;j++) {
                if(arr[i] == arr[j]*2)
                    return true;
            }              
        }
        return false;       
    }
}
```
