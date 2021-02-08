```
public class Solution {
    public int[] PlusOne(int[] digits) {
        digits[digits.Length - 1] = digits[digits.Length - 1] + 1;
        
        if(digits[digits.Length - 1] / 10 >= 1){
            for(int i = digits.Length - 1; i >=0; i--){
                if(digits[i] / 10 >= 1){
                    digits[i] = digits[i] - 10;
                    if(i - 1 < 0){
                        int temp = digits[0];
                        digits[0] = 1;
                        Array.Resize(ref digits, digits.Length + 1);
                        digits[1] = temp;
                    }
                    else{
                        digits[i-1] = digits[i-1]+1;
                    }
                }
            }
        }
        return digits;
    }
}
```