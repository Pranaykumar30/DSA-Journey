# 📦 Space Complexity – DSA Day 2

## What is Space Complexity?

Space Complexity is the **total memory** an algorithm needs to run, including:

- Input storage (arrays, strings)
- Temporary/auxiliary variables
- Recursion stack (function calls)

---

## 🔍 Why Space Complexity Matters

- Crucial in memory-limited environments
- Helps optimize your code
- Used to trade off with time (e.g., memoization)

---

## 📘 Common Space Complexities

| Notation   | Meaning         | Example Use Case                |
|------------|------------------|---------------------------------|
| O(1)       | Constant          | In-place operations             |
| O(n)       | Linear            | Using an array/list             |
| O(n²)      | Quadratic         | Using a matrix, 2D array        |
| O(log n)   | Logarithmic       | Binary recursion call stack     |

---

## 🔧 Examples

### O(1)
```python
def increment(arr):
    count = 0
    for i in arr:
        count += i
```

### O(n)
```python
def duplicate(arr):
    return arr[:]  # copies input
```

### O(n²)
```python
matrix = [[0]*n for _ in range(n)]
```

### 🔁 Recursion = Stack Space
Example: factorial(n)
Each call waits → memory used grows:

```python
factorial(4) → factorial(3) → factorial(2) → ...
```
Each level adds one frame to the stack → Total space: O(n)

### 🧠 Tips
- Prefer in-place changes if possible

- Be cautious of deep recursion (use loops or tail recursion)

### 🧾 Visual Aid
Recursion tree showing factorial(n) stack growth



### ✅ Summary
- Always consider memory alongside speed

- Practice estimating space in problems with arrays, recursion, DP