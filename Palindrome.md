## Palindrome Number

### Problem Statement
Given an integer `x`, return `true` if `x` is a palindrome, and `false` otherwise.

### Examples
#### Example 1:
**Input:**
```plaintext
x = 121
```
**Output:**
```plaintext
true
```
**Explanation:** 121 reads as 121 from left to right and from right to left.

#### Example 2:
**Input:**
```plaintext
x = -121
```
**Output:**
```plaintext
false
```
**Explanation:** From left to right, it reads -121. From right to left, it becomes 121-. Therefore, it is not a palindrome.

#### Example 3:
**Input:**
```plaintext
x = 10
```
**Output:**
```plaintext
false
```
**Explanation:** Reads 01 from right to left. Therefore, it is not a palindrome.

### Constraints
- `-2^{31} <= x <= 2^{31} - 1`

### Approach
#### C++ Approach
1. Convert the integer to a string.
2. Use two pointers: one at the start and one at the end of the string.
3. Compare characters from both ends moving towards the center.
4. If any mismatch is found, return `false`.
5. If the loop completes without mismatches, return `true`.

### Code Implementation (C++) (basic approach)
```cpp
class Solution {
public:
    bool isPalindrome(int x) {
        string y = to_string(x);
        int j = y.length() - 1;
        for(int i = 0; i < (y.length())/2; i++) {
            if(y[i] != y[j]) {
                return false;
            }
            j--;
        }
        return true;
    }
};
```

### Complexity Analysis
- **Time Complexity:** `O(n)`, where `n` is the number of digits in `x`.
- **Space Complexity:** `O(n)`, due to string conversion and storage.




### Code Implementation (C++) (optimized approach)
```cpp
class Solution {
public:
    bool isPalindrome(int x) {
        string y = to_string(x);
        int j = y.length() - 1;
        for(int i = 0; i < (y.length())/2; i++) {
            if(y[i] != y[j]) {
                return false;
            }
            j--;
        }
        return true;
    }
};
```

### Complexity Analysis
- **Time Complexity:** `O(n)`, where `n` is the number of digits in `x`.
- **Space Complexity:** `O(n)`, due to string conversion and storage.
