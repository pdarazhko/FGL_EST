```class Solution {
public int removeElement(int[] nums, int val) {
int i = 0; //1

        //3 2 2 3    3
        //0 1 2 3
        for(int j = 0; j < nums.length; j++) { //2 < 3
            if (nums[j] != val) {              //2 != 2
                nums[i] = nums[j];             //3 2 
                i++;
            }
        }
        
        return i;
    }
}
```