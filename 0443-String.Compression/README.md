# 443. String Compression

Given an array of characters, compress it in-place.

The length after compression must always be smaller than or equal to the
original array.

Every element of the array should be a __character__ (not int) of length 1.

After you are done __modifying the input array__ in-place, return the new length
of the array.
 
__Follow up:__

Could you solve it using only O(1) extra space?

__Example 1:__

```
Input:
["a","a","b","b","c","c","c"]

Output:
Return 6, and the first 6 characters of the input array should be: ["a","2","b","2","c","3"]

Explanation:
"aa" is replaced by "a2". "bb" is replaced by "b2". "ccc" is replaced by "c3".
```

__Example 2:__

```
Input:
["a"]

Output:
Return 1, and the first 1 characters of the input array should be: ["a"]

Explanation:
Nothing is replaced.
``` 

__Example 3:__

```
Input:
["a","b","b","b","b","b","b","b","b","b","b","b","b"]

Output:
Return 4, and the first 4 characters of the input array should be: ["a","b","1","2"].

Explanation:
Since the character "a" does not repeat, it is not compressed. "bbbbbbbbbbbb" is replaced by "b12".
Notice each digit has it's own entry in the array.
``` 

__Note:__

* All characters have an ASCII value in `[35, 126]`.
* `1 <= len(chars) <= 1000`.

__Hint:__

How do you know if you are at the end of a consecutive group of characters?
