# ⏱️ Time Complexity – DSA Day 2

## 🔍 What is Time Complexity?

Time Complexity is a way to describe **how the time of an algorithm scales** with the size of the input (`n`). It tells us the **growth rate**, not actual runtime.

---

## 🧠 Big O Notation

Big O describes the **worst-case** growth of time as input increases.

| Notation     | Meaning            | Example Use Case               |
|--------------|--------------------|--------------------------------|
| O(1)         | Constant            | Accessing array element        |
| O(log n)     | Logarithmic         | Binary search                  |
| O(n)         | Linear              | Iterating over array           |
| O(n log n)   | Linearithmic        | Merge sort, Quick sort (avg)   |
| O(n²)        | Quadratic           | Nested loops                   |
| O(2ⁿ)        | Exponential         | Recursion in subset generation |
| O(n!)        | Factorial           | Brute force permutations       |

---

## 🧾 Examples in Code

### O(1)
```python
arr = [1, 2, 3]
print(arr[0])
```
### O(n)
```python
for i in range(n):
    print(i)
```
### O(n²)
```python
for i in range(n):
    for j in range(n):
        print(i, j)
```
### O(log n)
```python
# Binary Search
while low <= high:
    mid = (low + high) // 2
```

## 📏 How to Analyze Complexity
* Remove constants → O(2n) = O(n)

* Focus on the highest term → O(n² + n) = O(n²)

* Consider loops, recursion, branching

## 📊 Visual Chart
![Big-O Notation]("E:/dsa_journey/Week-01-Foundation/Visuals/big_o_chart_day2.png")

## ✅ Summary

* Time Complexity ≠ real time

* It shows scalability

* Helps you choose the most optimal algorithm before writing code
