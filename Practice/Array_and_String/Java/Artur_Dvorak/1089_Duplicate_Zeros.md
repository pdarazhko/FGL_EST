```class Solution {
public void duplicateZeros(int[] arr) {
int i = 0;
int arrLength = arr.length;

        while (i < arrLength) {
            if (arr[i] == 0) {
                
                //shift
                for (int j = arrLength -1; j > i; j--) {
                    arr[j] = arr[j-1];
                }
                
                //duplicate
                if (i < arrLength-1) {
                    arr[i+1]=0;
                }
                i++;
            } 
            i++;
        }      
    }
}
```