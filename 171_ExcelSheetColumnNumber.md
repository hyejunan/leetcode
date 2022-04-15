### 171. Excel Sheet Column Number

***Easy***

Given a fixed-length integer array arr, duplicate each occurrence of zero, shifting the remaining elements to the right.

Note that elements beyond the length of the original array are not written. 
Do the above modifications to the input array in place and do not return anything.

```Java
class Solution {
    public int titleToNumber(String columnTitle) {
        int res = 0;
        for(int i = 0;i<columnTitle.length();i++) {
            res = res*26;
            res = res + (columnTitle.charAt(i) - 'A' + 1);
        }
        return res;
    }
}
```
