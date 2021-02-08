```public class Solution {
    public static void main(String[] args) {
        String s = "abccccdd";
        System.out.println(longestPalindrome(s));
    }

    public static int longestPalindrome(String s) {
        int[] count = new int[128];
        for (char c: s.toCharArray())
            count[c]++;

        int result = 0;

        for(int v: count) {
            result +=v/2*2;
            if (result % 2 == 0 && v % 2 == 1) result++;
        }

        return result;
    }
}
```