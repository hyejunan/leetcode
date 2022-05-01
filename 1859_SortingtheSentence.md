### 1859. Sorting the Sentence

***Easy***

Given a fixed-length integer array arr, duplicate each occurrence of zero, shifting the remaining elements to the right.

Note that elements beyond the length of the original array are not written. 
Do the above modifications to the input array in place and do not return anything.

```Java
class Solution {
    public String sortSentence(String s) {
        String []ans = new String[s.split(" ").length];
        for(String st: s.split(" ")){
            ans[st.charAt(st.length()-1) - '1'] = st.substring(0,st.length()-1);
        }
        return String.join(" ", ans);
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Sorting the Sentence.
Memory Usage: 39.9 MB, less than 98.64% of Java online submissions for Sorting the Sentence.
