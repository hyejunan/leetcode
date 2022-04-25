### 1773. Count Items Matching a Rule

***Easy***

You are given an array items, where each items[i] = [typei, colori, namei] describes the type, color, and name of the ith item. You are also given a rule represented by two strings, ruleKey and ruleValue.

The ith item is said to match the rule if one of the following is true:

ruleKey == "type" and ruleValue == typei.
ruleKey == "color" and ruleValue == colori.
ruleKey == "name" and ruleValue == namei.
Return the number of items that match the given rule.

```Java
class Solution {
    public int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
        int cnt = 0;
         switch(ruleKey) {
            case "type":
                 for(int i=0;i<items.size();i++) {
                     if(items.get(i).get(0).equals(ruleValue)) {
                         cnt++;
                     }
                 }
                 break;
            case "color":
                 for(int i=0;i<items.size();i++) {
                     if(items.get(i).get(1).equals(ruleValue)) {
                         cnt++;
                     }
                 }
                 break;
            case "name":
                 for(int i=0;i<items.size();i++) {
                     if(items.get(i).get(2).equals(ruleValue)) {
                         cnt++;
                     }
                 }
                 break;
            default:
                 break;
        } 
    return cnt;
    }
}
```
Runtime: 3 ms, faster than 98.12% of Java online submissions for Count Items Matching a Rule.
Memory Usage: 47.2 MB, less than 81.86% of Java online submissions for Count Items Matching a Rule.
