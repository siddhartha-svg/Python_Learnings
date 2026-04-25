# Python List Functions — Complete Guide with Concepts & Examples

---

## What is a List?

A **list** is an ordered, mutable (changeable) collection that can hold items of any data type.

```python
fruits = ["apple", "banana", "cherry"]
numbers = [1, 2, 3, 4, 5]
mixed = [1, "hello", 3.14, True]
```

---

## 1. `append()` — Add a Single Item to the End

**Concept:** Adds one element at the end of the list. Modifies the list in place.

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)  # ['apple', 'banana', 'cherry']
```

> Use when you want to add one item at a time to the end.

---

## 2. `extend()` — Add Multiple Items to the End

**Concept:** Takes an iterable (list, tuple, string) and adds each element individually to the end.

```python
fruits = ["apple", "banana"]
more_fruits = ["cherry", "mango"]
fruits.extend(more_fruits)
print(fruits)  # ['apple', 'banana', 'cherry', 'mango']
```

> **Difference from `append()`:** `append(["cherry", "mango"])` would add the whole list as one element; `extend()` unpacks and adds each item.

```python
# append vs extend
a = [1, 2]
b = [1, 2]

a.append([3, 4])   # [1, 2, [3, 4]]
b.extend([3, 4])   # [1, 2, 3, 4]
```

---

## 3. `insert()` — Add Item at a Specific Position

**Concept:** Inserts an element at a given index. Existing elements shift to the right.

```python
fruits = ["apple", "banana", "cherry"]
fruits.insert(1, "mango")
print(fruits)  # ['apple', 'mango', 'banana', 'cherry']
```

> Index `0` = beginning, `-1` = before the last element.

```python
fruits.insert(0, "grape")   # Add at beginning
fruits.insert(-1, "kiwi")   # Add before last item
```

---

## 4. `remove()` — Remove First Occurrence by Value

**Concept:** Searches the list and removes the **first** matching element. Raises `ValueError` if not found.

```python
fruits = ["apple", "banana", "apple", "cherry"]
fruits.remove("apple")
print(fruits)  # ['banana', 'apple', 'cherry']
```

> Only removes the **first** match, not all occurrences.

```python
# Safe removal with check
if "banana" in fruits:
    fruits.remove("banana")
```

---

## 5. `pop()` — Remove Item by Index and Return It

**Concept:** Removes the element at the given index and **returns** it. Default index is `-1` (last item).

```python
fruits = ["apple", "banana", "cherry"]
removed = fruits.pop()
print(removed)  # 'cherry'
print(fruits)   # ['apple', 'banana']

# Remove by specific index
removed = fruits.pop(0)
print(removed)  # 'apple'
```

> Use `pop()` when you need to both **remove and use** the removed value.

---

## 6. `clear()` — Remove All Items

**Concept:** Empties the list completely. The list still exists but becomes `[]`.

```python
fruits = ["apple", "banana", "cherry"]
fruits.clear()
print(fruits)  # []
```

> Different from `del fruits` — `clear()` keeps the list object, `del` removes it entirely.

---

## 7. `index()` — Find the Index of an Item

**Concept:** Returns the index of the **first** occurrence of the specified value. Raises `ValueError` if not found.

```python
fruits = ["apple", "banana", "cherry", "banana"]
print(fruits.index("banana"))  # 1
```

> You can specify a start and end range:

```python
# index(value, start, end)
print(fruits.index("banana", 2))  # 3  (search from index 2 onwards)
```

---

## 8. `count()` — Count Occurrences of an Item

**Concept:** Returns how many times a value appears in the list.

```python
numbers = [1, 2, 3, 2, 2, 4, 2]
print(numbers.count(2))  # 4
print(numbers.count(5))  # 0
```

> Useful for checking duplicates or frequency of an element.

---

## 9. `sort()` — Sort the List In Place

**Concept:** Sorts the list in ascending order by default. Modifies the original list. Does **not** return a new list.

```python
numbers = [3, 1, 4, 1, 5, 9, 2]
numbers.sort()
print(numbers)  # [1, 1, 2, 3, 4, 5, 9]

# Descending order
numbers.sort(reverse=True)
print(numbers)  # [9, 5, 4, 3, 2, 1, 1]
```

> Sort strings alphabetically:

```python
fruits = ["banana", "apple", "cherry"]
fruits.sort()
print(fruits)  # ['apple', 'banana', 'cherry']
```

> Sort with a custom key:

```python
words = ["banana", "fig", "apple", "kiwi"]
words.sort(key=len)           # sort by length
print(words)  # ['fig', 'kiwi', 'apple', 'banana']
```

---

## 10. `sorted()` — Sort Without Modifying Original (Built-in Function)

**Concept:** Returns a **new sorted list**. The original list remains unchanged.

```python
numbers = [3, 1, 4, 1, 5]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # [1, 1, 3, 4, 5]
print(numbers)         # [3, 1, 4, 1, 5]  — unchanged
```

> **`sort()` vs `sorted()`:**
> | | `sort()` | `sorted()` |
> |---|---|---|
> | Modifies original | Yes | No |
> | Returns | `None` | New list |
> | Works on | Lists only | Any iterable |

---

## 11. `reverse()` — Reverse the List In Place

**Concept:** Reverses the order of elements in the list. Modifies the list directly.

```python
fruits = ["apple", "banana", "cherry"]
fruits.reverse()
print(fruits)  # ['cherry', 'banana', 'apple']
```

> To reverse without modifying the original, use slicing `[::-1]`:

```python
original = [1, 2, 3, 4, 5]
reversed_copy = original[::-1]
print(reversed_copy)  # [5, 4, 3, 2, 1]
print(original)       # [1, 2, 3, 4, 5]
```

---

## 12. `copy()` — Shallow Copy of the List

**Concept:** Returns a new list with the same elements. Changes to the copy do **not** affect the original (for flat lists).

```python
original = [1, 2, 3]
copy_list = original.copy()
copy_list.append(4)

print(original)   # [1, 2, 3]
print(copy_list)  # [1, 2, 3, 4]
```

> **Why not just `copy = original`?**

```python
a = [1, 2, 3]
b = a           # b points to the SAME list
b.append(4)
print(a)        # [1, 2, 3, 4]  — original also changed!
```

---

## 13. `len()` — Get the Length of the List (Built-in)

**Concept:** Returns the total number of elements in the list.

```python
fruits = ["apple", "banana", "cherry"]
print(len(fruits))  # 3

empty = []
print(len(empty))   # 0
```

---

## 14. `min()` and `max()` — Smallest and Largest Values (Built-in)

**Concept:** Returns the minimum or maximum value from the list.

```python
numbers = [3, 1, 4, 1, 5, 9, 2]
print(min(numbers))  # 1
print(max(numbers))  # 9

fruits = ["banana", "apple", "cherry"]
print(min(fruits))   # 'apple'   (alphabetically first)
print(max(fruits))   # 'cherry'  (alphabetically last)
```

---

## 15. `sum()` — Sum of All Elements (Built-in)

**Concept:** Returns the sum of all numeric elements in the list.

```python
numbers = [1, 2, 3, 4, 5]
print(sum(numbers))        # 15
print(sum(numbers, 10))    # 25  (10 is the starting value)
```

---

## 16. `list()` — Convert Other Types to a List (Built-in)

**Concept:** Creates a new list from any iterable (string, tuple, range, etc.).

```python
# From a string
chars = list("hello")
print(chars)  # ['h', 'e', 'l', 'l', 'o']

# From a tuple
tup = (1, 2, 3)
lst = list(tup)
print(lst)    # [1, 2, 3]

# From a range
nums = list(range(1, 6))
print(nums)   # [1, 2, 3, 4, 5]
```

---

## 17. `in` / `not in` — Check if Item Exists

**Concept:** Membership operators to check presence of an element.

```python
fruits = ["apple", "banana", "cherry"]

print("banana" in fruits)      # True
print("mango" in fruits)       # False
print("mango" not in fruits)   # True
```

---

## 18. List Slicing — Access a Portion of the List

**Concept:** Extract a sub-list using `[start:stop:step]`.

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

print(numbers[2:5])    # [2, 3, 4]       — index 2 to 4
print(numbers[:4])     # [0, 1, 2, 3]    — from beginning to index 3
print(numbers[5:])     # [5, 6, 7, 8, 9] — from index 5 to end
print(numbers[::2])    # [0, 2, 4, 6, 8] — every 2nd element
print(numbers[::-1])   # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0] — reversed
```

---

## 19. List Comprehension — Create Lists Efficiently

**Concept:** A concise way to build a new list by applying an expression to each item in an iterable.

```python
# Syntax: [expression for item in iterable if condition]

# Squares of numbers 1–5
squares = [x**2 for x in range(1, 6)]
print(squares)  # [1, 4, 9, 16, 25]

# Even numbers only
evens = [x for x in range(10) if x % 2 == 0]
print(evens)    # [0, 2, 4, 6, 8]

# Uppercase all fruits
fruits = ["apple", "banana", "cherry"]
upper = [f.upper() for f in fruits]
print(upper)    # ['APPLE', 'BANANA', 'CHERRY']
```

---

## 20. `enumerate()` — Loop with Index and Value (Built-in)

**Concept:** Returns index-value pairs when iterating over a list.

```python
fruits = ["apple", "banana", "cherry"]

for index, fruit in enumerate(fruits):
    print(index, fruit)
# 0 apple
# 1 banana
# 2 cherry

# Start index from 1
for index, fruit in enumerate(fruits, start=1):
    print(index, fruit)
# 1 apple
# 2 banana
# 3 cherry
```

---

## 21. `zip()` — Combine Multiple Lists (Built-in)

**Concept:** Pairs elements from multiple lists together.

```python
names = ["Alice", "Bob", "Charlie"]
scores = [85, 92, 78]

for name, score in zip(names, scores):
    print(f"{name}: {score}")
# Alice: 85
# Bob: 92
# Charlie: 78

# Create a list of tuples
pairs = list(zip(names, scores))
print(pairs)  # [('Alice', 85), ('Bob', 92), ('Charlie', 78)]
```

---

## 22. `map()` — Apply a Function to Each Element (Built-in)

**Concept:** Applies a function to every element and returns a map object (convert to list).

```python
numbers = [1, 2, 3, 4, 5]

squared = list(map(lambda x: x**2, numbers))
print(squared)  # [1, 4, 9, 16, 25]

# Convert strings to integers
str_nums = ["1", "2", "3"]
int_nums = list(map(int, str_nums))
print(int_nums)  # [1, 2, 3]
```

---

## 23. `filter()` — Filter Elements by Condition (Built-in)

**Concept:** Returns only elements for which the function returns `True`.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8]

evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)  # [2, 4, 6, 8]

# Filter words longer than 4 characters
words = ["hi", "hello", "hey", "greetings"]
long_words = list(filter(lambda w: len(w) > 4, words))
print(long_words)  # ['hello', 'greetings']
```

---

## Quick Reference Table

| Function / Method | Purpose | Modifies Original? | Returns |
|---|---|---|---|
| `append(x)` | Add item to end | Yes | `None` |
| `extend(iterable)` | Add multiple items | Yes | `None` |
| `insert(i, x)` | Add at index | Yes | `None` |
| `remove(x)` | Remove first match | Yes | `None` |
| `pop(i)` | Remove & return by index | Yes | Removed item |
| `clear()` | Remove all items | Yes | `None` |
| `index(x)` | Find index of value | No | Index (int) |
| `count(x)` | Count occurrences | No | Count (int) |
| `sort()` | Sort in place | Yes | `None` |
| `sorted()` | Sort, return new list | No | New list |
| `reverse()` | Reverse in place | Yes | `None` |
| `copy()` | Shallow copy | No | New list |
| `len()` | Number of items | No | Count (int) |
| `min()` | Smallest element | No | Min value |
| `max()` | Largest element | No | Max value |
| `sum()` | Sum of elements | No | Sum value |
| `list()` | Convert to list | No | New list |
| `enumerate()` | Index + value pairs | No | Enumerate obj |
| `zip()` | Combine lists | No | Zip obj |
| `map()` | Apply function | No | Map obj |
| `filter()` | Filter by condition | No | Filter obj |

---

## Summary of Key Concepts

- **In-place methods** (`sort`, `reverse`, `append`, etc.) modify the original list and return `None`.
- **Non-modifying built-ins** (`sorted`, `len`, `min`, `max`) return a value without changing the list.
- **List comprehensions** are the Pythonic way to build filtered/transformed lists.
- Always use `.copy()` when you want an independent copy of a list.
- `pop()` is preferred over `remove()` when you know the index and need the removed value.
