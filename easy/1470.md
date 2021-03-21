# [Shuffle the Array](https://leetcode.com/problems/shuffle-the-array/)

```python
class Solution:
    def shuffle(self, nums: List[int], n: int) -> List[int]:
        result = []
        for i in range(n):
            result.extend([nums[i],nums[n+i]])
        return result
```



## Explanation

The aim of the question is to find a way to pair up the numbers in the array. For example,

[1,2,3,4] => [1,3,2,4]

To solve this, we know that array size is 2n. Hence first half of the array is [0..n-1] and next half to [n..2n-1]. To pair

Position 0 = 0,n

Position 1 = 0+1,n+1

Position 2 = 0+2, n+3

Position n-1= 0+n-1, n+n-1

Hence, we loop from 0..n-1 then add the pair to result.

```python
        for i in range(n):
            result.extend([nums[i],nums[n+i]])
```



