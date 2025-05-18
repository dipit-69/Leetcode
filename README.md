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
