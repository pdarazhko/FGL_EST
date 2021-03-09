```class Solution {
public int[] replaceElements(int[] arr) {
//17 18 5 4 6 1
//0  1  2 3 4 5
int right = arr.length-2; //4            
int max = arr[right+1]; //arr[5]=1

        while (right >= 0) { //3 >= 0
            int temp = arr[right]; //arr[3]=4

            for (int i = right; i < arr.length-1; i++) { //i=3; 3<5 
                if (arr[i+1] > max) //6>6
                    max = arr[i]; 
            }
            
            arr[right] = max; //arr[3]=1
            if (temp > max) 
                max = temp; //6
            right--; //3
        }
        
        arr[arr.length-1] = -1; 
        return arr;
    
```