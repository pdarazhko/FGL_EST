```

public class Solution {
    public bool IsPalindrome(ListNode head) {
    	var values = new List<int>();
    	while(head != null)
    	{
    		values.Add(head.val);
    		head = head.next;
    	}

    	var array = values.ToArray();
    	int low = 0;
    	int high = array.Length - 1;
    	while(low < high)
    	{
    		if(array[low] != array[high])
    		{
    			return false;
    		}
    		low++;
    		high--;
    	}
    	return true;
    }
}

```