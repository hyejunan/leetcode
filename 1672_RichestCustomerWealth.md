### 1672. Richest Customer Wealth

***Easy***

You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the i​​​​​​​​​​​th​​​​ customer has in the j​​​​​​​​​​​th​​​​ bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

```Java
class Solution {
    public int maximumWealth(int[][] accounts) {
        int m = accounts.length;
        int n = accounts[0].length;
        int temp = 0;
        int wealth = 0;
        
        for(int i =0;i<m;i++) {
            for(int j=0;j<n;j++) {
                temp += accounts[i][j];
            }
            if(wealth < temp)
                wealth = temp;
            temp = 0;
        }
        return wealth;
    }
}
```
