#[1791. Find Center of Star Graph](https://leetcode.com/problems/find-center-of-star-graph/)

One of the main challenge of this is how do we  find commonality between any 2 edges. Given 2 edges;

```python
edges = [[1,2],[5,1],[1,3],[1,4]]
```

Between 2 edges ```[1,2]``` and ```[5,1]```, we just need to find the potential intersection between them which in this case is 1. Then think about the edge cases

### Potential Edge Cases

- [2,2] and [2,2]. Our solution will still work because 2 will still be the answer.



## Solution

```python
class Solution:
    def findCenter(self, edges: List[List[int]]) -> int:
        return list(set(edges[0]) & set(edges[1]))[0]
```



