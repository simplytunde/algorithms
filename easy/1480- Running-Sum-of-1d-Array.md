#[1480. Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/)



### First Implementation

O(n)

```python
class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        return [ sum(nums[0:i+1]) for i in range(len(nums))]
```

### Second Implementation

```python
class Solution:
    def runningSum(self, nums: List[int]) -> List[int]:
        result = []
        currentSum = 0
        for n in nums:
            currentSum += n
            result.append(currentSum)
        return result
            
```

The second implementatin is faster than the first 