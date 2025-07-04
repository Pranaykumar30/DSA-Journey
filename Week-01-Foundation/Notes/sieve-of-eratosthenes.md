# 🔢 Sieve of Eratosthenes — DSA Day 3

---

## ✅ Goal

Find all prime numbers strictly less than `n` in O(n log log n) time.

---

## 🧠 Why It Works

- Mark all multiples of primes as `False` in a boolean array
- Start from `i * i` to skip already marked numbers
- Only go up to `√n` since higher multiples are handled by smaller primes

---

## 🧾 Dry Run Example (n = 10)

Initial:
`[False, False, True, True, True, True, True, True, True, True]`

After i = 2:
`[False, False, True, True, False, True, False, True, False, True]`

After i = 3:
`[False, False, True, True, False, True, False, True, False, False]`

Result = `[2, 3, 5, 7]`

---

## ✅ LeetCode-style Implementation

```python
class Solution:
    def countPrimes(self, n: int) -> int:
        if n <= 2:
            return 0

        is_prime = [True] * n
        is_prime[0] = is_prime[1] = False

        for i in range(2, int(n**0.5) + 1):
            if is_prime[i]:
                for j in range(i*i, n, i):
                    is_prime[j] = False

        return sum(is_prime)
```

### 📈 Time & Space Complexity

| Metric           | Value          |
| ---------------- | -------------- |
| Time Complexity  | O(n log log n) |
| Space Complexity | O(n)           |
