```/**
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
  public ListNode getIntersectionNode1(ListNode headA, ListNode headB) {
  ListNode pointerA = headA;
  ListNode pointerB = headB;

       while (pointerA != pointerB) {
           if (pointerA == null) pointerA = headB;
              else pointerA = pointerA.next;
           
           if (pointerB == null) pointerB = headA;
               else pointerB = pointerB.next;
       }
       
       return pointerA;
  }

  public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
  Set<ListNode> nodesInB = new HashSet<ListNode>();

       while (headB != null) {
           nodesInB.add(headB);
           headB = headB.next;
       }
       
       while (headA != null) {
           if (nodesInB.contains(headA)) {
               return headA;
           }
           headA = headA.next;
       }
       
       return null;

  }
  }
```