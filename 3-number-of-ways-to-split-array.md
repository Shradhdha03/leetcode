
https://leetcode.com/problems/number-of-ways-to-split-array

```python
class Solution:
    def waysToSplitArray(self, nums: List[int]) -> int:
        res = 0
        post = sum(nums)
        pre = 0
        for i in range(0, len(nums)-1):
            pre += nums[i] 
            post -= nums[i]
            if pre >= post:
                res += 1
        return res
        
```