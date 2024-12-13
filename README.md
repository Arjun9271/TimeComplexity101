# Time Complexity Cheat Sheet

This README provides a comprehensive guide to time complexity for various operations and loops in Python. Understanding these complexities is essential for writing efficient code.

---

## 1. **Time Complexity for Basic Operations**

### a. Arithmetic Operations

- Addition, subtraction, multiplication, division: **O(1)**
- Modulus, exponentiation: **O(1)**

### b. Comparisons

- Equality (`==`), less than (`<`), greater than (`>`), etc.: **O(1)**

### c. Variable Assignment

- Assigning a value to a variable: **O(1)**

### d. Accessing Elements

- Accessing an element in a list by index: **O(1)**
- Accessing a value in a dictionary by key: **O(1)**
- Accessing an element in a tuple by index: **O(1)**

---

## 2. **Time Complexity of Data Structure Operations**

### a. List

| Operation               | Time Complexity |
| ----------------------- | --------------- |
| Indexing (list[i])      | O(1)            |
| Appending (list.append) | O(1)            |
| Inserting (list.insert) | O(n)            |
| Deleting by index       | O(n)            |
| Iterating over a list   | O(n)            |
| Searching (using `in`)  | O(n)            |
| Sorting (list.sort)     | O(n \* log n)   |

### b. Dictionary

| Operation                      | Time Complexity |
| ------------------------------ | --------------- |
| Accessing a value by key       | O(1)            |
| Inserting a key-value pair     | O(1)            |
| Updating a value by key        | O(1)            |
| Deleting a key-value pair      | O(1)            |
| Iterating over all keys/values | O(n)            |

### c. Set

| Operation            | Time Complexity |
| -------------------- | --------------- |
| Adding an element    | O(1)            |
| Removing an element  | O(1)            |
| Checking membership  | O(1)            |
| Iterating over a set | O(n)            |

### d. Tuple

| Operation              | Time Complexity |
| ---------------------- | --------------- |
| Accessing by index     | O(1)            |
| Iterating over a tuple | O(n)            |

---

## 3. **Time Complexity of Loops**

### a. Single Loop

```python
for i in range(n):
    # O(1) operation
```

- Complexity: **O(n)**

### b. Nested Loops

```python
for i in range(n):
    for j in range(m):
        # O(1) operation
```

- Complexity: **O(n \* m)**
  - If , then **O(n^2)**

### c. Loops with Break

```python
for i in range(n):
    if condition:
        break
```

- Worst-case complexity: **O(n)**
- Best-case complexity: **O(1)** (if `break` occurs early)

### d. Loops with Skipping (e.g., `continue`)

- Complexity: Depends on the number of iterations effectively executed, typically **O(n)**.

---

## 4. **Time Complexity of Recursive Functions**

### a. Linear Recursion

```python
def func(n):
    if n == 0:
        return
    func(n - 1)
```

- Complexity: **O(n)**

### b. Binary Recursion

```python
def func(n):
    if n <= 1:
        return
    func(n - 1)
    func(n - 1)
```

- Complexity: **O(2^n)**

### c. Divide-and-Conquer

```python
def func(n):
    if n <= 1:
        return
    func(n // 2)
```

- Complexity: **O(log n)**

---

## 5. **Common Algorithmic Complexities**

| Complexity Class | Example Scenarios                    |
| ---------------- | ------------------------------------ |
| O(1)             | Accessing elements in a list or dict |
| O(log n)         | Binary search                        |
| O(n)             | Iterating through a list             |
| O(n \* log n)    | Efficient sorting (merge sort, etc.) |
| O(n^2)           | Nested loops                         |
| O(2^n)           | Recursive problems with branching    |

---

## 6. **General Guidelines for Optimization**

1. **Avoid Nested Loops**:

   - Try to flatten nested iterations where possible.

2. **Use Built-In Functions**:

   - Python's built-in functions (like `min`, `max`, `sum`, etc.) are highly optimized.

3. **Leverage Dictionaries and Sets**:

   - For membership checks and unique element handling, use dictionaries or sets for  operations instead of lists.

4. **Precompute Results**:

   - Avoid redundant computations inside loops by precomputing values.
# Time Complexity Order

This document provides a list of common time complexities in ascending order along with their symbols.

## Time Complexities in Ascending Order

1. **O(1)** - Constant time
   - The algorithm takes the same constant time regardless of the input size.
   
2. **O(log n)** - Logarithmic time
   - The algorithm's time grows logarithmically with the input size.
   
3. **O(n)** - Linear time
   - The algorithm's time grows linearly with the input size.

4. **O(n log n)** - Log-linear time
   - The algorithm’s time grows as the product of the input size and its logarithm.

5. **O(n²)** - Quadratic time
   - The algorithm's time grows quadratically with the input size.

6. **O(n³)** - Cubic time
   - The algorithm's time grows cubically with the input size.

7. **O(2^n)** - Exponential time
   - The algorithm’s time doubles with each additional input element.

8. **O(n!)** - Factorial time
   - The algorithm's time grows factorially with the input size.

## Conclusion

Understanding time complexities helps in analyzing the efficiency of algorithms. Algorithms with lower time complexities (e.g., O(1), O(log n)) are generally more efficient, especially for large inputs.


---

This README serves as a quick reference to time complexity for common operations and coding patterns in Python. Understanding these principles will help you write more efficient and scalable code!



