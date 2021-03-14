```

public class Solution {
    // 1 -> 2 -> 3 -> 4
    public ListNode ReverseList(ListNode head) {
        ListNode prev = null; // null
        
        while(head != null){ 
            ListNode nextNode = head.next; //2
            head.next = prev; // null
            prev = head; // 1
            head = nextNode; 
        }
        return prev;
    }
}

```