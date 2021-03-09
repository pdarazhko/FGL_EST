```class Solution {
public void moveZeroes(int[] nums) {
if (nums.length == 0 || nums == null) return;

        int r = nums.length-1;
        int l = 0;
        
        while (r >= 0) {
            //1 != 0
            if (nums[r]!=0) {
                r=r-1;
            } else {
                l = r;
                r=r-1; 
                while (l < nums.length-1) {
                    nums[l] = nums[l+1]; //
                    nums[l+1] = 0; //
                    l=l+1; //
                }
            }
        }
        
    }
}
```