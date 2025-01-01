```java
class Solution {
    public int maxScore(String s) {
        int zeros = 0;
        int ones = 0;

        for (char c : s.toCharArray()){
            if (c == '1'){
                ones++;
            }
        }
        int res = 0;
        for (int i =0; i < (s.length()-1) ; i++){
            if (s.charAt(i) == '0'){
                zeros++;
            } else {
                ones--;
            }
            res = Math.max(res, zeros+ones);
        }
        return res;
    }
}
```

```python
class Solution:
    def maxScore(self, s: str) -> int:
        
        zeros = 0
        ones = s.count("1")
        res = 0
        for i in range(len(s)-1):
            if s[i] == "0":
                zeros += 1
            else:
                ones -= 1
            res = max(res, zeros + ones)
 
        return res
```