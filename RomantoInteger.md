### 13. Roman to Integer

***Easy***

Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M.

For example, 2 is written as II in Roman numeral, just two one's added together. 12 is written as XII, which is simply X + II. The number 27 is written as XXVII, which is XX + V + II.

Roman numerals are usually written largest to smallest from left to right. However, the numeral for four is not IIII. Instead, the number four is written as IV. Because the one is before the five we subtract it making four. The same principle applies to the number nine, which is written as IX. There are six instances where subtraction is used:

I can be placed before V (5) and X (10) to make 4 and 9. 
X can be placed before L (50) and C (100) to make 40 and 90. 
C can be placed before D (500) and M (1000) to make 400 and 900.
Given a roman numeral, convert it to an integer.

```JavaScript
/**
 * @param {string} s
 * @return {number}
 */
var romanToInt = function(s) {
    var arr1 = ["I","V","X","L","C","D","M"];
    var arr2 = [1, 5, 10, 50, 100, 500, 1000];
    var splitArr = s.split('');
    var res = 0;
    for(var i=0;i<s.length;i++) {
        var add = 0;
        var chk = arr1.indexOf(splitArr[i])-arr1.indexOf(splitArr[i+1]);
        if (chk == -1 || chk == -2) {
            add = arr2[arr1.indexOf(splitArr[i+1])] - arr2[arr1.indexOf(splitArr[i])];                  i++;
        }
        else
            add = arr2[arr1.indexOf(splitArr[i])];
        res = res+ add;
    }
    return res;
};
```
