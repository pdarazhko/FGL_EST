```class Solution {
public int findMaxConsecutiveOnes(int[] nums) {
int max = 0;
int result = 0;
if (nums.length < 1) return result;

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] == 1) { 
                if (result == max) result++;
                max++;
            } else {
                if (max > result) result = max;
                max = 0;   
            }
        }
        return result;
    }
}
```