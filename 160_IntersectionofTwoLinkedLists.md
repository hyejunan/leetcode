### 160. Intersection of Two Linked Lists

***Easy***

Given the heads of two singly linked-lists headA and headB, return the node at which the two lists intersect. 
If the two linked lists have no intersection at all, return null.

```Java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
        HashSet<ListNode> set1 = new HashSet<ListNode>();
        if(headA == null || headB == null)
            return null;
        while(headA != null) {
            set1.add(headA);
            headA = headA.next;
        }
        while(headB != null) {
            if(set1.contains(headB))
                return headB;
            headB = headB.next;
        }
        return null;
    }
}
```
