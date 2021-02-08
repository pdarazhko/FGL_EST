```public class Solution {
    public int[] TwoSum(int[] nums, int target) {
        var hash = new Dictionary<int, int>();
        for(int i = 0; i< nums.Length; i++){
            if(hash.ContainsKey( target - nums[i] )){
                return new int[]{hash[target - nums[i]], i};
            }
            hash.Add(nums[i], i);
        }
        return new int[]{};
    }
}
```