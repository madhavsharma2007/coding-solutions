# Palindrome Number

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

Given an integer `x`, return `true` if `x` is a  **palindrome**, and `false` otherwise.

 

 **Example 1:** 

```
Input: x = 121
Output: true
Explanation: 121 reads as 121 from left to right and from right to left.

```

 **Example 2:** 

```
Input: x = -121
Output: false
Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.

```

 **Example 3:** 

```
Input: x = 10
Output: false
Explanation: Reads 01 from right to left. Therefore it is not a palindrome.

```

 

 **Constraints:** 

- -231 <= x <= 231 - 1

 

 **Follow up:**  Could you solve it without converting the integer to a string?

## Solution

**Language:** Python  
**Runtime:** 16 ms (beats 42.55%)  
**Memory:** 12 MB (beats 92.28%)  
**Submitted:** 2026-11-07T00:47:01.625Z  

```py
class Solution(object):
    def isPalindrome(self, x):
        if x < 0:
            return False
        
        num = x
        result = 0

        while num > 0:
            last_digit = num % 10
            result = result * 10 + last_digit
            num //= 10
        
        return x == result

        
```

---

[View on LeetCode](https://leetcode.com/problems/palindrome-number/)