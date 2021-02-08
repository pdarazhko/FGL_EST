```
public class Solution {
    public int LongestPalindrome(string s) 
        {   
            int result = 0;
            var hash = new Dictionary<char, int>();
            foreach (var ch in s){
                if(hash.ContainsKey(ch)){
                    hash[ch]++;
                } else {
                    hash[ch] = 1;
                }
            }

            foreach (var pair in hash)
                {   
                    result += (pair.Value / 2) * 2;
                    if (result % 2 == 0 && pair.Value % 2 == 1)
                    {
                        result++;
                    }
                }
            return result;
        }
}
```
