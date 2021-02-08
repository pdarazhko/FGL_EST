```
public class Solution {
    public bool RotateString(string A, string B) {
      string doubled = String.Concat(A,A);
      return ( doubled.Contains(B) && A.Length == B.Length );
    }
}
```