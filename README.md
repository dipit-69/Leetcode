# LeetCode Solutions

---

## 🧠 Problem: 1768. Merge Strings Alternately

**Link:** [LeetCode Problem 1768](https://leetcode.com/problems/merge-strings-alternately/)

### 💬 Question:

![Question](https://github.com/dipit-69/Leetcode/blob/main/que1.jpg?raw=true)

You are given two strings `word1` and `word2`. Merge the strings by adding letters in alternating order, starting with `word1`. If a string is longer than the other, append the additional letters onto the end of the merged string.

#### Examples:

* Input: `word1 = "abc", word2 = "pqr"` → Output: `"apbqcr"`
* Input: `word1 = "ab", word2 = "pqrs"` → Output: `"apbqrs"`
* Input: `word1 = "abcd", word2 = "pq"` → Output: `"apbqcd"`

---

### ✅ Solution (Python):

![Solution Code](https://github.com/dipit-69/Leetcode/blob/main/sol1.jpg?raw=true)

---

## 🧠 Problem 2: Products that are Both Low Fat and Recyclable

### 💬 Question:

You are given a `Products` table with columns `product_id`, `low_fats`, and `recyclable`. Both `low_fats` and `recyclable` are ENUM values that can be `'Y'` or `'N'`.

Your task is to find all product IDs for which both `low_fats` and `recyclable` are `'Y'`.

#### Example:

| product_id | low_fats | recyclable |
|------------|----------|------------|
| 0          | Y        | N          |
| 1          | Y        | Y          |
| 2          | N        | Y          |
| 3          | Y        | Y          |
| 4          | N        | N          |

Output should be:

| product_id |
|------------|
| 1          |
| 3          |

---

### ✅ Solution (SQL):

```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y' AND recyclable = 'Y';
🧠 Problem 3: Customers Not Referred by Customer with ID 2
💬 Question:
You have a Customer table with id, name, and referee_id columns. The referee_id refers to the customer who referred them.

Find all customer names who are not referred by the customer with id = 2. This includes customers who were not referred by anyone (referee_id is NULL) and those referred by customers other than 2.

Example:
id	name	referee_id
1	Will	NULL
2	Jane	NULL
3	Alex	2
4	Bill	NULL
5	Zack	1
6	Mark	2

Output should be:

name
Will
Jane
Bill
Zack

✅ Solution (SQL):
sql
Copy
Edit
SELECT name
FROM Customer
WHERE referee_id IS NULL OR referee_id <> 2;
🧠 Problem 4: Greatest Common Divisor of Strings
💬 Question:
Given two strings str1 and str2, return the largest string x such that x divides both str1 and str2.

We say that string t divides string s if s is formed by concatenating t one or more times.

Examples:
Input: str1 = "ABCABC", str2 = "ABC" → Output: "ABC"

Input: str1 = "ABABAB", str2 = "ABAB" → Output: "AB"

Input: str1 = "LEET", str2 = "CODE" → Output: ""

✅ Solution (Python):
python
Copy
Edit
class Solution:
    def gcd(self, a, b):
        while b:
            a, b = b, a % b
        return a

    def gcdOfStrings(self, str1, str2):
        # Get gcd of lengths
        gcd_len = self.gcd(len(str1), len(str2))
        
        # Candidate divisor string
        candidate = str1[:gcd_len]
        
        # Check if candidate divides both str1 and str2
        if candidate * (len(str1) // gcd_len) == str1 and candidate * (len(str2) // gcd_len) == str2:
            return candidate
        else:
            return ""

# Test cases
solution = Solution()
print(solution.gcdOfStrings("ABCABC", "ABC"))    # Output: "ABC"
print(solution.gcdOfStrings("ABABAB", "ABAB"))   # Output: "AB"
print(solution.gcdOfStrings("LEET", "CODE"))     # Output: ""
Screenshots
Merge Strings Alternately
Question:

Solution:
