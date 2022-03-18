### 83. Remove Duplicates from Sorted List

***Easy***

Given the head of a sorted linked list, delete all duplicates such that each element appears only once. Return the linked list sorted as well.

````Java
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
    public ListNode deleteDuplicates(ListNode head) {
        ListNode p = head;
        if(head==null || head.next==null)
            return head;
        while(p!=null&&p.next!=null) {
            if(p.val == p.next.val)
                p.next = p.next.next;
            else
                p = p.next;
        }
        return head;
    }
}
