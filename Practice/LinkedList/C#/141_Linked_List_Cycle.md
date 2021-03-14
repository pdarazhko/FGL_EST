```

public class Solution {
    public bool HasCycle(ListNode head) {
    
        if(head == null || head.next == null){
            return false;
        }
        
        ListNode slow = head; //3
        ListNode fast = head; //3
        
        while(fast != null && fast.next != null){ // 2 != null || 0 != null
            
            slow = slow.next; // 0
            fast = fast.next.next; // 2

            if(slow == fast){ // 0 == 2
                return true;
            }
        }
        return false;
    }

}

```