```public class Solution {
    public static void main(String[] args) {
        String A = "abcde";
        String B = "cdeab";
        System.out.println(rotateString1(A, B));
    }

    public static boolean rotateString1(String A, String B) { //Brute Force
        if (A.length() != B.length()) return false;
        if (A.length() == 0) return true;

        search:
        for (int s = 0; s < A.length(); ++s) {
            for (int i = 0; i < A.length(); ++i) {
                if (A.charAt((s+i) % A.length()) != B.charAt(i))
                    continue search;
            }
            return true;
        }
        return false;
    }

    private static boolean rotateString(String A, String B, int rotation) {
        for(int i = 0; i < A.length(); i++) {
            if(A.charAt(i) != B.charAt((i+rotation)%B.length())) {
                return false;
            }
        }
        return true;
    }

    public static boolean rotateString2(String A, String B) { //Simple Check
        return A.length() == B.length() && (A+A).contains(B);
    }
}
```