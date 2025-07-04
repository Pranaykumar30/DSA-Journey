# 🔁 GCD & LCM — DSA Day 4

---

## 🔢 GCD (Greatest Common Divisor)

The largest number that divides both `a` and `b`.

### ✅ Euclidean Algorithm

```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a
```

### 🔄 Dry Run: `gcd(24, 18)`

| Step | a  | b  | a % b |
|------|----|----|--------|
| 1    | 24 | 18 | 6      |
| 2    | 18 | 6  | 0      |
| ✅   | 6  | 0  | done   |

**Answer:** GCD(24, 18) = 6

---

## 📈 Time Complexity
- O(log(min(a, b))): extremely fast

---

## 🔁 LCM (Least Common Multiple)

The smallest number that is divisible by both `a` and `b`.

### 🧠 Formula:
```python
LCM(a, b) = (a * b) // GCD(a, b)
```

### ✅ Code:
```python
def lcm(a, b):
    return (a * b) // gcd(a, b)
```

### ✍️ Example:
```python
LCM(4, 6) = (4×6) // GCD(4,6) = 24 // 2 = 12
```

---

## 🌍 Real-Life Applications
- Reducing fractions
- Rotations/cyclic patterns
- Scheduling problems
- Modular inverse calculation

---

## 🧪 Combined Example
```python
a, b = 12, 18
g = gcd(a, b)       # 6
l = lcm(a, b)       # 36
print(g, l)         # Output: 6 36
```