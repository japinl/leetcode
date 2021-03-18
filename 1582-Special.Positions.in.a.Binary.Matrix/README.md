# 1582. Special Positions in a Binary Matrix

Given a `rows x cols` matrix `mat`, where `mat[i][j]` is either `0` or
`1`, return _the number of special positions_ in `mat`.

A position `(i,j)` is called __special__ if `mat[i][j] == 1` and all
other elements in row `i` and column `j` are `0` (rows and columns are
__0-indexed__).

__Example 1:__

```
Input: mat = [[1,0,0],
              [0,0,1],
              [1,0,0]]
Output: 1
Explanation: (1,2) is a special position because mat[1][2] == 1 and all other elements in row 1 and column 2 are 0.
```

__Example 2:__

```
Input: mat = [[1,0,0],
              [0,1,0],
              [0,0,1]]
Output: 3
Explanation: (0,0), (1,1) and (2,2) are special positions. 
```

__Example 3:__

```
Input: mat = [[0,0,0,1],
              [1,0,0,0],
              [0,1,1,0],
              [0,0,0,0]]
Output: 2
```

__Example 4:__

```
Input: mat = [[0,0,0,0,0],
              [1,0,0,0,0],
              [0,1,0,0,0],
              [0,0,1,0,0],
              [0,0,0,1,1]]
Output: 3
```

__Constraints:__

* `rows == mat.length`
* `cols == mat[i].length`
* `1 <= rows, cols <= 100`
* `mat[i][j]` is `0` or `1`.
