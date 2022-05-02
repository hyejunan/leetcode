### 1221. Split a String in Balanced Strings

***Easy***

Balanced strings are those that have an equal quantity of 'L' and 'R' characters.

Given a balanced string s, split it in the maximum amount of balanced strings.

Return the maximum amount of split balanced strings.
```Java
class Solution {
    public int balancedStringSplit(String s) {
        int cnt = 0;
        int res = 0;
        for(char c: s.toCharArray()) {
            cnt = cnt + (c == 'R' ? 1 : -1);
            if(cnt == 0)
                res++;
        }
        return res;
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Split a String in Balanced Strings.
Memory Usage: 40.4 MB, less than 78.52% of Java online submissions for Split a String in Balanced Strings.
