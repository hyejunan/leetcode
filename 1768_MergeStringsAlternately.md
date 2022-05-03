### 1768. Merge Strings Alternately

***Easy***

You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. 
If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.

```Java
class Solution {
    public String mergeAlternately(String word1, String word2) {
        int len1 = word1.length();
        int len2 = word2.length();
        char[] res = new char[len1+len2];
        int j = 0;
        int k = 0;
        for(int i=0;i<len1+len2;){
            if(j<len1){
                res[i++] = word1.charAt(j++); 
            }
            if(k<len2) {
                res[i++] = word2.charAt(k++);
            }
        }
        return new String(res);
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Merge Strings Alternately.
Memory Usage: 40.3 MB, less than 96.09% of Java online submissions for Merge Strings Alternately.
