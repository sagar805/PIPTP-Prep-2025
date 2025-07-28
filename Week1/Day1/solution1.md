```Problem 1
``` Pseudocode:
def fun(w, x):
    y = 0
    if ((x % w == 0) or (w % x) == 0):
        y = y + 1
    else:
        y = y + 10
    print(y)

print(fun(40, 4))
```

### Step-by-step Analysis:

1. **Function Definition**: `fun(w, x)` takes two parameters.

2. **Initialize `y`**:

   ```python
   y = 0
   ```

3. **Conditional Check**:

   ```python
   if ((x % w == 0) or (w % x) == 0):
   ```

   This condition checks:

   * `x % w == 0`: Is `x` divisible by `w`?
   * `w % x == 0`: Is `w` divisible by `x`?

   **Given:** `fun(40, 4)`

   * `x = 4`, `w = 40`
   * `4 % 40 == 4` → **False**
   * `40 % 4 == 0` → **True**

   Since one of the conditions is `True`, the entire condition is `True` (due to the `or`).

4. **Then Block Executes**:

   ```python
   y = y + 1  # y becomes 1
   ```

5. **Print Statement**:

   ```python
   print(y)  # prints 1
   ```

6. **Return Value**:

   * The function doesn't explicitly return anything → Python returns `None` by default.

7. **Final Output**:

   * First prints `1` (from `print(y)`)
   * Then prints `None` (from `print(fun(40, 4))`)

---

### **Output:**

```
1
None
```







``` Problem 2



### Pseudocode:

```
 Integer a
 Set a = 1
 while (a < 5)
     a = a + 2
 end while
 Print a
```

---

### Step-by-step Execution:

* **Initial value**: `a = 1`
* **Condition**: `a < 5` → `1 < 5` → ✅ **True**

  * Inside loop: `a = 1 + 2 = 3`

---

* **Second iteration**: `a = 3`
* **Condition**: `3 < 5` → ✅ **True**

  * Inside loop: `a = 3 + 2 = 5`

---

* **Third iteration**: `a = 5`
* **Condition**: `5 < 5` → ❌ **False**

  * Loop terminates

---

### ✅ Final answer:

* The loop runs **2 times**

``` Problem 3


### 🔹 Pseudocode 
```python
def funn(a, b):
    if (a and b and a + b > 0):
        return a + funn(a - 2, b - 2) + b
    return a ^ b
```

---

### ✅ Base case:

The recursive call happens only when:

* `a ≠ 0`
* `b ≠ 0`
* `a + b > 0`

Otherwise, it returns `a ^ b` (bitwise XOR).

---

### 🔁 Evaluate step-by-step:

Let's trace it:

#### Step 1:

```
funn(8, 8)
→ 8 + funn(6, 6) + 8
```

#### Step 2:

```
funn(6, 6)
→ 6 + funn(4, 4) + 6
```

#### Step 3:

```
funn(4, 4)
→ 4 + funn(2, 2) + 4
```

#### Step 4:

```
funn(2, 2)
→ 2 + funn(0, 0) + 2
```

#### Base Case:

```
funn(0, 0) → 0 ^ 0 = 0
```

---

### 🧮 Backtrack the values:

Now substitute back:

```
funn(2,2) = 2 + 0 + 2 = 4
funn(4,4) = 4 + 4 + 4 = 12
funn(6,6) = 6 + 12 + 6 = 24
funn(8,8) = 8 + 24 + 8 = 40
```

---

### ✅ Final Answer:

**Output = 40** ✅

``` problem 4


### 📜 Pseudocode:

```
 Integer a, b
 Set a = 3, b = 3
 a = b
 if (1 ^ 1)
      a = 1
 Else
     b = 2
 End if
 Print a + b
```

---

### 🧠 Explanation:

* Line 2: `a = 3`, `b = 3`

* Line 3: `a = b` → both still `3`

* Line 4: `if (1 ^ 1)`

  * `1 ^ 1` is **bitwise XOR** of 1 and 1 → `0` (since 1 XOR 1 = 0)
  * So, the **condition is False**

* Line 6-7: Else block executes → `b = 2`

Now:

* `a = 3`
* `b = 2`

---

### ✅ Final Step:

```python
Print a + b = 3 + 2 = 5
```

---

### ✅ Final Answer:

5 

``` Problem 5


### 📜 **Pseudocode
```python
function funn(a, b):
    for c from 2 to 4:  # Inclusive range: 2, 3, 4
        if (a % 2 < b % 3):
            a = 4 % 3
        else:
            if (5 % 3 > b):
                a = b
            b = 1
    return a + b
```

Let's run this logic for a test case, e.g., **`a = 7, b = 5`** (same as earlier image-based question).

---

### 🧠 Initial Values:

* `a = 7`
* `b = 5`

---

### 🔁 Loop `c = 2 to 4` (i.e., 3 iterations)

---

### ✅ **Iteration 1 (c = 2):**

* `a % 2 = 1`
* `b % 3 = 2`
* `1 < 2` → ✅ True
  → `a = 4 % 3 = 1`

Now: `a = 1`, `b = 5`

---

### ✅ **Iteration 2 (c = 3):**

* `a % 2 = 1`
* `b % 3 = 2`
* `1 < 2` → ✅ True
  → `a = 4 % 3 = 1` (remains same)

---

### ✅ **Iteration 3 (c = 4):**

* `a % 2 = 1`
* `b % 3 = 2`
* `1 < 2` → ✅ True
  → `a = 4 % 3 = 1` (again)

---

### 🔚 After loop:

* `a = 1`
* `b = 5`

→ Return `a + b = 1 + 5 = 6`

---

### ✅ Final Answer:

**6**







