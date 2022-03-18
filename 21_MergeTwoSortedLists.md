### 21. Merge Two Sorted Lists

***Easy***

Merge two sorted linked lists and return it as a sorted list. The list should be made by splicing together the nodes of the first two lists.

```
Input: l1 = [1,2,4], l2 = [1,3,4]
Output: [1,1,2,3,4,4]
```

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
    public ListNode mergeTwoLists(ListNode l1, ListNode l2) {
        if(l1==null && l2==null)
            return null;
        if(l1==null||l2==null)
            return l1 == null ? l2 : l1;
        ListNode head = new ListNode();
        ListNode curr = head;
        while(l1!=null&&l2!=null) {
            if(l1.val == l2.val) {
                head.next = new ListNode(l1.val);
                head = head.next;
                head.next = new ListNode(l2.val);
                l1 = l1.next;
                l2 = l2.next;
            }
            else if(l1.val > l2.val) {
                head.next = new ListNode(l2.val);
                l2 = l2.next;
            }
            else {
                head.next = new ListNode(l1.val);
                l1 = l1.next;
            }
            head = head.next;
        }
        if(l1!=null)
            head.next = l1;
        if(l2!=null)
            head.next = l2;
        return curr.next;
    }
}
```
