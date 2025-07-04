# 🔢 Modular Arithmetic (Mod + Power) — DSA Day 4

---

## ✅ Concept

Modular arithmetic is used to perform calculations **under a fixed number system (mod m)**. It’s the foundation of hashing, number theory, cryptography, and more.

---

## 🧠 Key Properties (mod m)

| Expression           | Rule                          |
|---------------------|-------------------------------|
| (a + b) % m         | = ((a % m) + (b % m)) % m     |
| (a - b) % m         | = ((a % m) - (b % m) + m) % m |
| (a * b) % m         | = ((a % m) * (b % m)) % m     |

---

## 🧪 Example: `3^4 % 5`

1. Calculate `3^4 = 81`
2. `81 % 5 = 1`
3. ✅ Answer: **1**

But this is **not efficient**. Instead, we use binary exponentiation.

---

## 🚀 Modular Exponentiation (Binary Exponentiation)

```python
def modular_exponentiation(a, b, m):
    result = 1
    a = a % m

    while b > 0:
        if b % 2 == 1:
            result = (result * a) % m
        a = (a * a) % m
        b = b // 2

    return result
```

---

### 🧾 Dry Run: `modular_exponentiation(3, 4, 5)`

| Step | a | b | result | action                         |
|------|---|---|--------|--------------------------------|
| init | 3 | 4 | 1      | a % 5                          |
| 1    | 4 | 2 | 1      | a = (3×3)%5 = 4                |
| 2    | 1 | 1 | 1      | a = (4×4)%5 = 1                |
| 3    | 1 | 0 | 1      | result = (1×1)%5 = 1 (b odd)   |

✅ Output: `1`

---

## 📈 Time and Space Complexity

| Metric           | Value       |
|------------------|-------------|
| Time Complexity  | O(log b)    |
| Space Complexity | O(1)        |

---

## ✅ Applications
- Cryptography (RSA, Fermat's Theorem)
- Combinatorics (modulo factorials)
- CP number theory problems
- Avoiding overflow in big products

---

📌 Use when you see `a^b % m` in constraints like `1 ≤ b ≤ 1e9`
