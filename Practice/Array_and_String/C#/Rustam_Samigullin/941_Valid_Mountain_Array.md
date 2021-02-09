```
public class Solution {
    public bool ValidMountainArray(int[] arr) {
        if(arr.Length < 3){
            return false;
        }
        int left = 0;
        int right = arr.Length - 1;
        while(left < arr.Length-1 && arr[left] < arr[left+1]){
            left++;
        }
        while(right > 0 && arr[right] < arr[right-1]){
            right--;
        }
        
        if(left != right || right == 0 || left == arr.Length - 1){
            return false;
        }
        return true;        
    }
}
```