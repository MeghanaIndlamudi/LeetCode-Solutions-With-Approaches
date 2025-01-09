## [Leetcode 151: Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)

### Approaches:
- [Approach 1: Using Built-in Functions](#approach-1-using-built-in-functions)

### Approach 1: Using Built-in Functions

**Intuition:**

This approach leverages built-in Java functions to split the string by spaces, remove any empty elements, and reverse the resulting word list. This is straightforward but relies heavily on library functions.

**Steps:**
1. Split the input string by spaces.
2. Filter out any empty strings resulting from extra spaces.
3. Reverse the list and join the words into a single string with space separation.

```java
class Solution {
    public String reverseWords(String s) {
        // Step 1: Split the input string on spaces
        String[] words = s.trim().split("\\s+");
        
        // Step 2: Use StringBuilder to construct the result efficiently
        StringBuilder reversed = new StringBuilder();
        for (int i = words.length - 1; i >= 0; i--) {
            reversed.append(words[i]);
            if (i != 0) {
                reversed.append(" ");
            }
        }
        
        return reversed.toString();
    }
}
```

**Time Complexity:** O(N), where N is the length of the input string, due to splitting and joining operations.

**Space Complexity:** O(N), used by split and the StringBuilder.

---
