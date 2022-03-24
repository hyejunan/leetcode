### 876. Middle of the Linked List

***Easy***

Given the head of a singly linked list, return the middle node of the linked list.

If there are two middle nodes, return the second middle node.

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
    public ListNode middleNode(ListNode head) {
        ListNode fast = head;
        ListNode slow = head;
        while(fast.next != null && fast.next.next != null) {
            slow = slow.next;
            fast = fast.next.next;
        }
        if(fast.next!=null)
            slow = slow.next;
        ListNode res = slow;
        return res;
    }
}
```
