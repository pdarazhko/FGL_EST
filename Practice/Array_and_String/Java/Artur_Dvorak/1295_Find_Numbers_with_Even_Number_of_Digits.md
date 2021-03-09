```class Solution {
public int findNumbers(int[] nums) {
if (nums.length < 1) return 0;
int result = 0;

        for (int i = 0; i < nums.length; i++) {
            if ((numberOfDigits(nums[i]) % 2) == 0) result++;
        }
        
        return result;
    }
    
    public int numberOfDigits(int num) {
        return (int) (Math.log10(num) + 1);
    }
}
```