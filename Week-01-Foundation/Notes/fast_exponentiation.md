# ⚡ Fast Exponentiation (Binary Exponentiation) — DSA Day 5

---

## ✅ Problem
Compute large powers like `a^b` efficiently, especially when `b` is very large.

---

## 🚫 Naive Method
```python
def power(a, b):
    result = 1
    for _ in range(b):
        result *= a
    return result
```
⛔ Time Complexity: O(b)

Too slow when `b = 10^9`

---

## ⚡ Fast Exponentiation (Binary Exponentiation)

### 🧠 Intuition:
Every integer can be broken into binary (powers of 2)

For example:
```
b = 13 = 1101 (in binary)
So:
a^13 = a^8 * a^4 * a^1
```
We compute powers of 2 using squaring:
- a, a^2, a^4, a^8, a^16 ...
Multiply those where the binary bit is `1`

---

## ✅ Code (Iterative)
```python
def fast_power(a, b):
    result = 1
    while b > 0:
        if b % 2 == 1:
            result *= a
        a *= a
        b //= 2
    return result
```

---

## 🔁 Dry Run: `fast_power(3, 5)`

```text
Initial: a = 3, b = 5, result = 1

Step 1: b = 5 (odd)
→ result = 1 * 3 = 3
→ a = 3 * 3 = 9
→ b = 2

Step 2: b = 2 (even)
→ a = 9 * 9 = 81
→ b = 1

Step 3: b = 1 (odd)
→ result = 3 * 81 = 243
→ a = 81 * 81 = 6561
→ b = 0 → done

✅ Output = 243
```

---

## 📈 Complexity
| Metric           | Value    |
|------------------|----------|
| Time Complexity  | O(log b) |
| Space Complexity | O(1)     |

---

## 🧠 Summary
| Concept                   | Insight                          |
|---------------------------|----------------------------------|
| Binary breakdown          | b = sum of powers of 2           |
| Efficient power build-up  | via squaring (a, a^2, a^4...)    |
| Conditional multiply      | if bit is `1`, multiply in result|

---

## 🔗 Use Cases
- Modular arithmetic
- Encryption (RSA)
- Number theory
- Efficient loops in competitive programming

---
