[389. Find the Difference](https://leetcode.com/problems/find-the-difference/)
==========================

原题
----

Given two string *s* and *t* which consist of only lowercase letters.

String *t* is generated by random shuffling string *s* and then add
one more letter at a random position.

Find the letter that was added in *t*.

**Example:**

```
Input:
s = "abcd"
t = "abcde"

Output:
e

Explanation:
'e' is the letter that was added.
```

题意
----

给定两个字符串 *s* 和 *t* ，它们都仅由小写字符组成。

字符串 *t* 是通过随机移动字符串 *s* 并且在任意位置添加额外一个字符组成
的。

找出字符串 *t* 中添加的字符。

**示例：**

```
输入：
s = "abcd"
t = "abcde"

输出：
e

解释：
'e' is the letter that was added.
```

1. 起初想到的办法是通过遍历字符串 *s* 建立一个表，该表用于标记字符串
   *s* 中出现的字符，接着在遍历字符串 *t* 判断字符是否已经在 *s* 中出
   现，若未出现，则认为是新添加的字符。该方案的问题在于字符串 *s* 和
   *t* 中出现的字符可以多次出现，例如 `s="abcd", t="abcda"`，此时应该
   返回字符`'a'`。显然这种方案不可行。
2. 注意到字符串 *t* 是由 字符串 *s* 打乱顺序后，并在随机选取一个位置加
   入一个字符，那么可以肯定的是字符串 *s* 中的字符至少在字符串 *s* 和
   *t* 中出现了两次，根据这个依据，我们可以采用异或解决该问题。

代码
----

思路2示例代码
```c++
class Solution {
public:
	char findTheDifference(string s, string t) {
		unsigned char ch = t[0];
		
		for (size_t i = 0; i < s.size(); ++i) {
			ch ^= s[i];
			ch ^= t[i + 1];
		}
		
		return ch;
	}
};
```