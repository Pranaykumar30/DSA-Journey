# 🧠 Bit Manipulation — DSA Day 5

---

## 💡 What is Bit Manipulation?
Bit manipulation is performing operations directly on the binary representation of numbers using bitwise operators.

---

## 🔢 Binary Representation
Every number is represented in base-2 (binary) internally:
```
5 → 101
6 → 110
```

---

## 🛠️ Core Bitwise Operators

| Operator      | Symbol | Binary Example        | Decimal Result | Description                |
|---------------|--------|------------------------|----------------|----------------------------|
| AND           | `&`    | 5 & 3 = 101 & 011 = 001 | 1              | Bit is 1 if both are 1     |
| OR            | `|`    | 5 | 3 = 101 | 011 = 111 | 7              | Bit is 1 if either is 1    |
| XOR           | `^`    | 5 ^ 3 = 101 ^ 011 = 110 | 6              | Bit is 1 if bits differ    |
| NOT           | `~`    | ~5 = -6                |                | Inverts bits               |
| Left Shift    | `<<`   | 5 << 1 = 1010          | 10             | Multiplies by 2            |
| Right Shift   | `>>`   | 5 >> 1 = 10            | 2              | Divides by 2               |

---

## ✅ Common Bitwise Tricks

### ✔️ Check if number is Odd or Even
```python
if n & 1:
    print("Odd")
else:
    print("Even")
```

### ✔️ Multiply and Divide by 2
```python
n << 1   # n * 2
n >> 1   # n // 2
```

### ✔️ Swap two numbers (no temp)
```python
a = a ^ b
b = a ^ b
a = a ^ b
```

### ✔️ Count Set Bits (Brian Kernighan's Algorithm)
```python
def countSetBits(n):
    count = 0
    while n:
        n = n & (n - 1)
        count += 1
    return count
```

---

## 🧠 Real-Life Use Cases
- Competitive programming (speed)
- Game state encoding (on/off states)
- Subsets & bitmask DP
- Low-level optimization

---

## 📈 Time Complexity
| Operation Type     | Time       |
|--------------------|------------|
| Bitwise Ops        | O(1)       |
| Count Set Bits     | O(log n)   |

---

## 🧾 Summary Table
| Task                          | Code                         |
|-------------------------------|------------------------------|
| Check odd/even                | `n & 1`                      |
| Multiply by 2                 | `n << 1`                     |
| Divide by 2                   | `n >> 1`                     |
| Count set bits                | Brian Kernighan’s algorithm  |
| Swap two variables            | XOR Swap                     |

---
