### 1816. Truncate Sentence

***Easy***

A sentence is a list of words that are separated by a single space with no leading or trailing spaces. Each of the words consists of only uppercase and lowercase English letters (no punctuation).

For example, "Hello World", "HELLO", and "hello world hello world" are all sentences.
You are given a sentence s​​​​​​ and an integer k​​​​​​. You want to truncate s​​​​​​ such that it contains only the first k​​​​​​ words. Return s​​​​​​ after truncating it.

```Java
class Solution {
    public String truncateSentence(String s, int k) {
        for (int i = 0; i < s.length(); ++i) {
            if (s.charAt(i) == ' ' && --k == 0) {
                return s.substring(0, i);
            }
        }
        return s;
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Truncate Sentence.
Memory Usage: 40.3 MB, less than 97.34% of Java online submissions for Truncate Sentence.

