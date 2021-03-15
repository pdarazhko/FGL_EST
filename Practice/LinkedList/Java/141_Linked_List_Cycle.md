```/**
* Definition for singly-linked list.
* class ListNode {
*     int val;
*     ListNode next;
*     ListNode(int x) {
*         val = x;
*         next = null;
*     }
* }
  */
  public class Solution {
  public boolean hasCycle1(ListNode head) {
  if (head == null) return false;

       ListNode slow = head;
       ListNode fast = head;
       
       while (fast != null && fast.next != null) {            
           slow = slow.next;
           fast = fast.next.next;
           if (fast == slow) return true;
       }
       
       return false;
  }

  public boolean hasCycle(ListNode head) {
  Set<ListNode> visited = new HashSet<ListNode>();

       while (head != null) {
           if (visited.contains(head)) return true;
           visited.add(head);
           head = head.next;
       }
       
       return false;
  }
  }
```