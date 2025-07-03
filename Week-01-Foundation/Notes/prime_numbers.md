# 🔢 Prime Numbers – DSA Day 3

---

## ✅ What is a Prime Number?

A **prime number** is a number **greater than 1** that is divisible only by **1 and itself**.

| ✅ Prime | ❌ Not Prime |
|----------|-------------|
| 2, 3, 5, 7, 11 | 4, 6, 9, 15 (divisible by others) |

---

## ❗ Why Are Prime Numbers Important in DSA?

- Foundational in **Sieve of Eratosthenes**
- Used in **modular arithmetic**
- Fundamental to **GCD, LCM, Factorization**
- Widely used in **Cryptography (RSA)**

---

## 🔍 Naive Prime Check – O(n)

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
```
🚫 Not scalable. Too slow for large inputs.

### ⚡ Optimized Prime Check – O(√n)

```python
import math

def is_prime_optimized(n):
    if n <= 1:
        return False
    for i in range(2, int(math.sqrt(n)) + 1):
        if n % i == 0:
            return False
    return True
```

### ✅ Sample Outputs

```python
print(is_prime_optimized(11))  # True
print(is_prime_optimized(21))  # False
```

### 📈 Time Complexity Visual
Comparison of operations between:

- Naive Check → O(n)

- Optimized Check → O(√n)

![image](https://github.com/user-attachments/assets/bde5008c-1335-4582-b4a7-d990840e4513)


### 🧠 Tips
- Always use O(√n) method for competitive coding

- Prime checks appear in number theory, DP, hashing problems

- Avoid writing sieve manually unless needed

### 🔚 Summary

| Method    | Time Complexity |
| --------- | --------------- |
| Naive     | O(n)            |
| Optimized | O(√n)           |
