``` 

public class Solution {
    public int GetDecimalValue(ListNode head) {
        if(head.next == null){
            return head.val;
        }
        
        String result = "";
        
        while(head != null){
            result+=head.val;
            head = head.next;
        }
        
        Console.WriteLine(result);
        
        return Convert.ToInt32(result, 2);
        
    }
}


```