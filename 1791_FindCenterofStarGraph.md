### 1791. Find Center of Star Graph

***Easy***

There is an undirected star graph consisting of n nodes labeled from 1 to n. A star graph is a graph where there is one center node and exactly n - 1 edges that connect the center node with every other node.

You are given a 2D integer array edges where each edges[i] = [ui, vi] indicates that there is an edge between the nodes ui and vi. Return the center of the given star graph.

```Java
class Solution {
    public int findCenter(int[][] e) {
        return e[0][0] == e[1][0] || e[0][0] == e[1][1] ? e[0][0] : e[0][1];
    }
}
```
Runtime: 0 ms, faster than 100.00% of Java online submissions for Find Center of Star Graph.
Memory Usage: 79.2 MB, less than 41.35% of Java online submissions for Find Center of Star Graph.

