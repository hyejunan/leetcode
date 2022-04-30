### 2181. Merge Nodes in Between Zeros

***Medium***

You are given the head of a linked list, which contains a series of integers separated by 0's. The beginning and end of the linked list will have Node.val == 0.

For every two consecutive 0's, merge all the nodes lying in between them into a single node whose value is the sum of all the merged nodes. The modified list should not contain any 0's.

Return the head of the modified linked list.

```Java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode mergeNodes(ListNode head) {
        ListNode curr, root = new ListNode();
        curr = root;
        int sum = 0;
        while(head != null){
            if(head.val == 0 && sum != 0){
                curr.next = new ListNode(sum);
                curr = curr.next;
                sum = 0;   
            }
            sum += head.val;
            head = head.next;
        }
        return root.next;
    }
    
}
```
Runtime: 8 ms, faster than 77.71% of Java online submissions for Merge Nodes in Between Zeros.
Memory Usage: 80.6 MB, less than 82.46% of Java online submissions for Merge Nodes in Between Zeros.
