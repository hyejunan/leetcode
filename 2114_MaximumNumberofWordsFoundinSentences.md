### 2114. Maximum Number of Words Found in Sentences

***Easy***

A sentence is a list of words that are separated by a single space with no leading or trailing spaces.

You are given an array of strings sentences, where each sentences[i] represents a single sentence.

Return the maximum number of words that appear in a single sentence.

```Java
class Solution {
    public int mostWordsFound(String[] sentences) {
        int cnt = 1;
        int temp = 0;
        
        for(String i:sentences) {
            for(int j=0;j<i.length();j++) {
                if(i.charAt(j) == ' ')
                    cnt++;
            }
            if(temp < cnt)
                temp = cnt;
            cnt = 1;
        }
        return temp;
    }
}
```
