# [1108. Defanging an IP Address](https://leetcode.com/problems/defanging-an-ip-address/)

```python
class Solution:
    def defangIPaddr(self, address: str) -> str:
        return address.replace(".","[.]")
```



## Explanation

The goal of the problem is to replace every `.` with `[.]` which is quite easy to do in python using the method `replace`



