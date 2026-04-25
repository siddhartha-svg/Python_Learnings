# Python String Functions — Complete Guide with Concepts & Examples

---

## What is a String?

A **string** is an ordered, immutable sequence of characters enclosed in single `' '`, double `" "`, or triple `''' '''` quotes.

```python
name = "Alice"
greeting = 'Hello, World!'
paragraph = """This is
a multi-line string."""
```

> **Immutable** means once created, a string cannot be changed — all string methods return a **new string**.

---

## 1. `len()` — Get the Length of a String

**Concept:** Returns the total number of characters (including spaces) in the string.

```python
text = "Hello, World!"
print(len(text))   # 13

print(len(""))     # 0
print(len("  "))   # 2  (spaces count)
```

---

## 2. `upper()` — Convert to Uppercase

**Concept:** Returns a new string with all characters converted to uppercase.

```python
text = "hello world"
print(text.upper())   # 'HELLO WORLD'

# Useful for case-insensitive comparisons
user_input = "yes"
if user_input.upper() == "YES":
    print("Confirmed!")
```

---

## 3. `lower()` — Convert to Lowercase

**Concept:** Returns a new string with all characters converted to lowercase.

```python
text = "HELLO WORLD"
print(text.lower())   # 'hello world'

# Normalize input for comparison
email = "User@Example.COM"
print(email.lower())  # 'user@example.com'
```

---

## 4. `capitalize()` — Capitalize First Letter

**Concept:** Returns a new string with the **first character** uppercased and the rest lowercased.

```python
text = "hello world"
print(text.capitalize())   # 'Hello world'

text2 = "PYTHON IS FUN"
print(text2.capitalize())  # 'Python is fun'
```

---

## 5. `title()` — Title Case Every Word

**Concept:** Capitalizes the **first letter of every word**.

```python
text = "hello world from python"
print(text.title())   # 'Hello World From Python'

name = "john doe"
print(name.title())   # 'John Doe'
```

---

## 6. `swapcase()` — Swap Upper and Lower Case

**Concept:** Converts uppercase to lowercase and vice versa for every character.

```python
text = "Hello World"
print(text.swapcase())   # 'hELLO wORLD'

text2 = "PyThOn"
print(text2.swapcase())  # 'pYtHoN'
```

---

## 7. `strip()` — Remove Leading & Trailing Whitespace

**Concept:** Removes whitespace (spaces, tabs, newlines) from both ends of the string.

```python
text = "   Hello World   "
print(text.strip())    # 'Hello World'

# With specific characters
text2 = "***Hello***"
print(text2.strip("*"))  # 'Hello'
```

> Related methods:
> - `lstrip()` — removes only from the **left**
> - `rstrip()` — removes only from the **right**

```python
text = "   Hello   "
print(text.lstrip())   # 'Hello   '
print(text.rstrip())   # '   Hello'
```

---

## 8. `replace()` — Replace Part of a String

**Concept:** Replaces all occurrences of a substring with another. Optionally limit the number of replacements.

```python
text = "I like cats. Cats are great. I have a cat."
print(text.replace("cat", "dog"))
# 'I like dogs. dogs are great. I have a dog.'

# Case-sensitive — 'Cats' is NOT replaced
print(text.replace("cat", "dog"))
# 'I like dogs. Cats are great. I have a dog.'

# Limit replacements to 1
print(text.replace("cat", "dog", 1))
# 'I like dogs. Cats are great. I have a cat.'
```

---

## 9. `find()` — Find Index of First Occurrence

**Concept:** Returns the index of the **first** occurrence of a substring. Returns `-1` if not found (does not raise an error).

```python
text = "Hello, World!"
print(text.find("World"))   # 7
print(text.find("Python"))  # -1

# Search within a range: find(sub, start, end)
print(text.find("o", 5))    # 8  (search from index 5)
```

---

## 10. `index()` — Find Index (Raises Error if Not Found)

**Concept:** Same as `find()`, but raises a `ValueError` if the substring is not found.

```python
text = "Hello, World!"
print(text.index("World"))   # 7

# Raises ValueError
# print(text.index("Python"))  # ValueError: substring not found
```

> **`find()` vs `index()`:**
> | | `find()` | `index()` |
> |---|---|---|
> | Not found | Returns `-1` | Raises `ValueError` |
> | Safe to use | Yes | Use with try/except |

---

## 11. `count()` — Count Occurrences of a Substring

**Concept:** Returns how many times a substring appears in the string.

```python
text = "banana"
print(text.count("a"))     # 3
print(text.count("an"))    # 2
print(text.count("xyz"))   # 0

# Count within a range
print(text.count("a", 2))  # 2  (from index 2 onwards)
```

---

## 12. `split()` — Split String into a List

**Concept:** Splits the string by a delimiter and returns a **list**. Default delimiter is whitespace.

```python
text = "apple banana cherry"
print(text.split())         # ['apple', 'banana', 'cherry']

# Split by specific delimiter
csv = "one,two,three,four"
print(csv.split(","))       # ['one', 'two', 'three', 'four']

# Limit splits
print(csv.split(",", 2))    # ['one', 'two', 'three,four']
```

---

## 13. `rsplit()` — Split from the Right

**Concept:** Same as `split()` but splits from the **right** side when a maxsplit is given.

```python
text = "one,two,three,four"
print(text.rsplit(",", 2))   # ['one,two', 'three', 'four']
```

---

## 14. `splitlines()` — Split by Line Breaks

**Concept:** Splits the string at line boundaries (`\n`, `\r\n`, etc.) and returns a list.

```python
text = "Line 1\nLine 2\nLine 3"
print(text.splitlines())
# ['Line 1', 'Line 2', 'Line 3']

multiline = """Hello
World
Python"""
print(multiline.splitlines())
# ['Hello', 'World', 'Python']
```

---

## 15. `join()` — Join a List into a String

**Concept:** Joins elements of an iterable into a single string using the string as the separator.

```python
words = ["apple", "banana", "cherry"]
print(", ".join(words))    # 'apple, banana, cherry'
print(" - ".join(words))   # 'apple - banana - cherry'
print("".join(words))      # 'applebananacherry'

# Join characters
chars = ["H", "e", "l", "l", "o"]
print("".join(chars))      # 'Hello'
```

---

## 16. `startswith()` — Check if String Starts With

**Concept:** Returns `True` if the string starts with the specified prefix.

```python
text = "Hello, World!"
print(text.startswith("Hello"))    # True
print(text.startswith("World"))    # False

# Check multiple prefixes using a tuple
filename = "report.pdf"
print(filename.startswith(("report", "summary")))  # True
```

---

## 17. `endswith()` — Check if String Ends With

**Concept:** Returns `True` if the string ends with the specified suffix.

```python
filename = "document.pdf"
print(filename.endswith(".pdf"))           # True
print(filename.endswith(".txt"))           # False

# Check multiple suffixes
print(filename.endswith((".pdf", ".docx")))  # True
```

---

## 18. `isdigit()` — Check if All Characters are Digits

**Concept:** Returns `True` if all characters in the string are digits (0–9).

```python
print("12345".isdigit())    # True
print("123.45".isdigit())   # False  (dot is not a digit)
print("12 34".isdigit())    # False  (space is not a digit)
print("".isdigit())         # False  (empty string)
```

---

## 19. `isalpha()` — Check if All Characters are Letters

**Concept:** Returns `True` if all characters are alphabetic (a–z, A–Z).

```python
print("Hello".isalpha())    # True
print("Hello123".isalpha()) # False
print("Hello World".isalpha())  # False  (space not allowed)
```

---

## 20. `isalnum()` — Check if All Characters are Letters or Digits

**Concept:** Returns `True` if all characters are alphanumeric (letters + digits, no spaces/symbols).

```python
print("Hello123".isalnum())   # True
print("Hello 123".isalnum())  # False  (space)
print("Hello!".isalnum())     # False  (!)
```

---

## 21. `isspace()` — Check if All Characters are Whitespace

**Concept:** Returns `True` if the string contains only whitespace characters.

```python
print("   ".isspace())    # True
print("\t\n".isspace())   # True
print("  a  ".isspace())  # False
```

---

## 22. `isupper()` / `islower()` — Check Case

**Concept:** Check whether all cased characters are uppercase or lowercase.

```python
print("HELLO".isupper())   # True
print("Hello".isupper())   # False

print("hello".islower())   # True
print("Hello".islower())   # False

print("HELLO 123".isupper())  # True  (digits are ignored)
```

---

## 23. `zfill()` — Pad with Zeros on the Left

**Concept:** Fills the string with leading zeros to reach the specified width.

```python
print("42".zfill(5))       # '00042'
print("hello".zfill(8))    # '000hello'
print("1234567".zfill(5))  # '1234567'  (no truncation if longer)
```

> Useful for formatting IDs, order numbers, etc.

---

## 24. `center()` / `ljust()` / `rjust()` — Align Text

**Concept:** Pads the string to a given width with a fill character (default: space).

```python
text = "Hello"

print(text.center(11))          # '   Hello   '
print(text.center(11, "-"))     # '---Hello---'

print(text.ljust(10))           # 'Hello     '
print(text.ljust(10, "."))      # 'Hello.....'

print(text.rjust(10))           # '     Hello'
print(text.rjust(10, "."))      # '.....Hello'
```

---

## 25. `format()` — String Formatting

**Concept:** Inserts values into placeholders `{}` inside the string.

```python
# Positional
print("Hello, {}! You are {} years old.".format("Alice", 30))
# 'Hello, Alice! You are 30 years old.'

# Keyword arguments
print("Name: {name}, Age: {age}".format(name="Bob", age=25))
# 'Name: Bob, Age: 25'

# Formatting numbers
print("Pi is approximately {:.2f}".format(3.14159))
# 'Pi is approximately 3.14'
```

---

## 26. f-Strings (Formatted String Literals) — Modern Formatting

**Concept:** Prefix `f` before a string to embed expressions directly inside `{}`.

```python
name = "Alice"
age = 30
print(f"Hello, {name}! You are {age} years old.")
# 'Hello, Alice! You are 30 years old.'

# Expressions inside f-strings
x = 5
print(f"Square of {x} is {x**2}")
# 'Square of 5 is 25'

# Format numbers
pi = 3.14159
print(f"Pi = {pi:.2f}")   # 'Pi = 3.14'
```

---

## 27. `encode()` — Encode String to Bytes

**Concept:** Converts a string to a bytes object using the specified encoding (default: `utf-8`).

```python
text = "Hello"
encoded = text.encode("utf-8")
print(encoded)         # b'Hello'
print(type(encoded))   # <class 'bytes'>

# Decode back to string
decoded = encoded.decode("utf-8")
print(decoded)         # 'Hello'
```

---

## 28. String Slicing — Extract Part of a String

**Concept:** Extract a portion of a string using `[start:stop:step]`.

```python
text = "Hello, World!"

print(text[0:5])     # 'Hello'
print(text[7:])      # 'World!'
print(text[:5])      # 'Hello'
print(text[-6:])     # 'orld!'
print(text[::2])     # 'Hlo ol!'  (every 2nd character)
print(text[::-1])    # '!dlroW ,olleH'  (reversed)
```

---

## 29. `in` / `not in` — Check Substring Membership

**Concept:** Check if a substring exists within a string.

```python
text = "Hello, World!"

print("World" in text)       # True
print("Python" in text)      # False
print("Python" not in text)  # True
```

---

## 30. `maketrans()` + `translate()` — Character Mapping

**Concept:** `maketrans()` creates a translation table; `translate()` applies it to replace/remove characters.

```python
# Replace characters
table = str.maketrans("aeiou", "12345")
text = "Hello World"
print(text.translate(table))   # 'H2ll4 W4rld'

# Remove characters (third arg = chars to delete)
table2 = str.maketrans("", "", "aeiou")
print("Hello World".translate(table2))   # 'Hll Wrld'
```

---

## 31. `partition()` — Split into Three Parts

**Concept:** Splits the string at the **first** occurrence of the separator, returning a tuple of 3 parts: `(before, separator, after)`.

```python
text = "Hello: World"
print(text.partition(":"))    # ('Hello', ':', ' World')

url = "https://example.com"
print(url.partition("://"))   # ('https', '://', 'example.com')
```

---

## 32. `rpartition()` — Split from the Right

**Concept:** Like `partition()` but splits at the **last** occurrence of the separator.

```python
text = "one:two:three"
print(text.partition(":"))    # ('one', ':', 'two:three')
print(text.rpartition(":"))   # ('one:two', ':', 'three')
```

---

## Quick Reference Table

| Method | Purpose | Returns |
|---|---|---|
| `len(s)` | Length of string | int |
| `upper()` | All uppercase | New string |
| `lower()` | All lowercase | New string |
| `capitalize()` | First letter capitalized | New string |
| `title()` | Each word capitalized | New string |
| `swapcase()` | Swap upper/lower | New string |
| `strip()` | Remove leading/trailing whitespace | New string |
| `lstrip()` | Remove left whitespace | New string |
| `rstrip()` | Remove right whitespace | New string |
| `replace(old, new)` | Replace substrings | New string |
| `find(sub)` | Index of first match (-1 if not found) | int |
| `index(sub)` | Index of first match (error if not found) | int |
| `count(sub)` | Count occurrences | int |
| `split(sep)` | Split into list | list |
| `rsplit(sep)` | Split from right | list |
| `splitlines()` | Split by line breaks | list |
| `join(iterable)` | Join list into string | New string |
| `startswith(prefix)` | Starts with check | bool |
| `endswith(suffix)` | Ends with check | bool |
| `isdigit()` | All digits? | bool |
| `isalpha()` | All letters? | bool |
| `isalnum()` | All letters or digits? | bool |
| `isspace()` | All whitespace? | bool |
| `isupper()` | All uppercase? | bool |
| `islower()` | All lowercase? | bool |
| `zfill(width)` | Zero-pad left | New string |
| `center(width)` | Center align | New string |
| `ljust(width)` | Left align | New string |
| `rjust(width)` | Right align | New string |
| `format(...)` | Format with placeholders | New string |
| `encode(enc)` | String → bytes | bytes |
| `partition(sep)` | Split into 3-tuple | tuple |
| `rpartition(sep)` | Split from right into 3-tuple | tuple |
| `maketrans()` + `translate()` | Character substitution/removal | New string |

---

## Summary of Key Concepts

- Strings are **immutable** — every method returns a **new string**, never changes the original.
- Use `f-strings` (Python 3.6+) for clean, readable string formatting.
- `find()` is safer than `index()` when you're unsure if a substring exists.
- `split()` + `join()` are opposites — convert between strings and lists.
- `strip()` is essential for cleaning user input or file-read data.
- Use `startswith()` / `endswith()` with tuples to check multiple conditions at once.
- Slicing `[start:stop:step]` works the same way on strings as on lists.
