
### 1. Area of a Rectangle

```python
# Area = length × breadth
length = float(input("Enter length: "))
breadth = float(input("Enter breadth: "))
area = length * breadth
print(f"Area of rectangle: {area}")
```

---

### 2. Simple Interest

```python
# SI = (P × R × T) / 100
P = float(input("Principal (P): "))
R = float(input("Rate % per annum (R): "))
T = float(input("Time in years (T): "))
SI = (P * R * T) / 100
print(f"Simple Interest: {SI}")
```

---

### 3. Positive, Negative, or Zero

```python
n = float(input("Enter a number: "))
if n > 0:
    print("Positive")
elif n < 0:
    print("Negative")
else:
    print("Zero")
```

---

### 4. Largest of Three Numbers

```python
a = float(input("First number: "))
b = float(input("Second number: "))
c = float(input("Third number: "))
largest = a
if b > largest:
    largest = b
if c > largest:
    largest = c
print(f"Largest number is: {largest}")
```

---

### 5. Leap Year Checker

```python
year = int(input("Enter year: "))
# Leap if divisible by 4, not by 100 unless also by 400
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year} is a leap year.")
else:
    print(f"{year} is not a leap year.")
```

---

### 6. Integer to Binary/Hex/Octal

```python
n = int(input("Enter an integer: "))
print(f"Binary: {bin(n)}")
print(f"Hexadecimal: {hex(n)}")
print(f"Octal: {oct(n)}")
```

---

### 7. Swap Variables Without a Third

```python
x = input("Enter first value: ")
y = input("Enter second value: ")
print(f"Before swap: x={x}, y={y}")
# Swap in one line
x, y = y, x
print(f"After swap:  x={x}, y={y}")
```

---

### 8. Reverse String (Slicing)

```python
s = input("Enter a string: ")
rev = s[::-1]
print(f"Reversed: {rev}")
```

---

### 9. Palindrome Check

```python
s = input("Enter a string: ")
if s == s[::-1]:
    print("Palindrome")
else:
    print("Not a palindrome")
```

---

### 10. Count Vowels & Consonants

```python
s = input("Enter text: ").lower()
vowels = "aeiou"
v_count = 0
c_count = 0
for ch in s:
    if ch.isalpha():
        if ch in vowels:
            v_count += 1
        else:
            c_count += 1
print(f"Vowels: {v_count}, Consonants: {c_count}")
```

---

### 11. Count Words in a Sentence

```python
sentence = input("Enter a sentence: ").strip()
words = sentence.split()
print(f"Word count: {len(words)}")
```

---

### 12. Filter Even Numbers from a List

```python
nums = input("Enter numbers separated by spaces: ").split()
# Convert to ints
nums = [int(n) for n in nums]
evens = [n for n in nums if n % 2 == 0]
print(f"Even numbers: {evens}")
```

---

### 13. Simple Stopwatch (using `time`)

```python
import time

input("Press ENTER to start the stopwatch")
start = time.time()
input("Press ENTER to stop the stopwatch")
end = time.time()
elapsed = end - start
print(f"Elapsed time: {elapsed:.2f} seconds")
```

---

### 14. Dice Simulator (two dice)

```python
import random

die1 = random.randint(1, 6)
die2 = random.randint(1, 6)
print(f"Die 1: {die1}, Die 2: {die2}, Total: {die1 + die2}")
```

---

### 15. Lottery Number Picker (6 unique from 1–49)

```python
import random

numbers = list(range(1, 50))
picks = random.sample(numbers, 6)
print("Your lottery numbers are:", sorted(picks))
```
