# 1200. Minimum Absolute Difference

Given an array of __distinct__ integers `arr`, find all pairs of elements with
the minimum absolute difference of any two elements. 

Return a list of pairs in ascending order(with respect to pairs), each pair
`[a, b]` follows

* `a`, `b` are from `arr`
* `a < b`
* `b - a` equals to the minimum absolute difference of any two elements in `arr`

__Example 1:__

```
Input: arr = [4,2,1,3]
Output: [[1,2],[2,3],[3,4]]
Explanation: The minimum absolute difference is 1. List all pairs with difference equal to 1 in ascending order.
```

__Example 2:__

```
Input: arr = [1,3,6,10,15]
Output: [[1,3]]
```

__Example 3:__

```
Input: arr = [3,8,-10,23,19,-4,-14,27]
Output: [[-14,-10],[19,23],[23,27]]
```

__Constraints:__

* `2 <= arr.length <= 10^5`
* `-10^6 <= arr[i] <= 10^6`
