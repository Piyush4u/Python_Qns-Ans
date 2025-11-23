# Python Exercises: Data Types, Operators, and Strings (No Conditionals or Loops)
---

## A. Arithmetic & Operators (1–25)

1. **Add Two Numbers**  
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print(a + b)
```

2. **Subtract Two Numbers**  
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print(a - b)
```

3. **Multiply Two Numbers**  
```python
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))
print(a * b)
```

4. **Divide Two Numbers (Quotient)**  
```python
a = int(input("Dividend: "))
b = int(input("Divisor: "))
print(a // b)
```

5. **Divide Two Numbers (Remainder)**  
```python
a = int(input("Dividend: "))
b = int(input("Divisor: "))
print(a % b)
```

6. **Exponentiation**  
```python
print(float(input("Base: ")) ** float(input("Exponent: ")))
```

7. **Floor Division**  
```python
print(int(input("a: ")) // int(input("b: ")))
```

8. **Modulus**  
```python
print(int(input("a: ")) % int(input("b: ")))
```

9. **Average of Three Numbers**  
```python
print((float(input()) + float(input()) + float(input())) / 3)
```

10. **Square of a Number**  
```python
n = float(input("Enter number: "))
print(n ** 2)
```

11. **Cube of a Number**  
```python
n = float(input("Enter number: "))
print(n ** 3)
```

12. **Circle Area (π=3.14)**  
```python
print(3.14 * float(input("Radius: ")) ** 2)
```

13. **Swap Variables**  
```python
x = input("x: "); y = input("y: ")
x, y = y, x
print(x, y)
```

14. **Increment by 1**  
```python
n = int(input("Enter integer: "))
n += 1
print(n)
```

15. **Decrement by 1**  
```python
n = int(input("Enter integer: "))
n -= 1
print(n)
```

16. **Compound Multiplication**  
```python
n = int(input("Enter integer: "))
n *= 2
print(n)
```

17. **Compound Division**  
```python
n = float(input("Enter number: "))
n /= 2
print(n)
```

18. **Negate a Number**  
```python
print(-float(input("Enter number: ")))
```

19. **Absolute Value**  
```python
n = float(input("Enter number: "))
print((n**2)**0.5)
```

20. **Percentage**  
```python
print((float(input("Part: ")) / float(input("Whole: "))) * 100)
```

21. **Circle Circumference (π=3.14)**  
```python
print(2 * 3.14 * float(input("Radius: ")))
```

22. **Power of 10**  
```python
print(int(input("Exponent: ")) * 10)
```

23. **String to Integer +5**  
```python
print(int(input("Enter digits: ")) + 5)
```

24. **Float to Int**  
```python
print(int(float(input("Enter float: "))))
```

25. **Chained Addition**  
```python
a, b, c = float(input()), float(input()), float(input())
print(a + b + c)
```

---

## B. String Operations (26–50)

26. **Length**  
```python
print(len(input("String: ")))
```

27. **Concatenate**  
```python
print(input("First: ") + input("Second: "))
```

28. **Repeat**  
```python
print(input("String: ") * 3)
```

29. **Uppercase**  
```python
print(input("String: ").upper())
```

30. **Lowercase**  
```python
print(input("String: ").lower())
```

31. **Swap Case**  
```python
print(input("String: ").swapcase())
```

32. **Title Case**  
```python
print(input("String: ").title())
```

33. **Count Substring**  
```python
s = input("String: ")
print(s.count(input("Substring: ")))
```

34. **Find Substring**  
```python
s = input("String: ")
print(s.find(input("Substring: ")))
```

35. **Is Digit**  
```python
print(input("String: ").isdigit())
```

36. **Is Alpha**  
```python
print(input("String: ").isalpha())
```

37. **Is Alnum**  
```python
print(input("String: ").isalnum())
```

38. **Strip**  
```python
print(input("String: ").strip())
```

39. **Lstrip**  
```python
print(input("String: ").lstrip())
```

40. **Rstrip**  
```python
print(input("String: ").rstrip())
```

41. **Center**  
```python
print(input("String: ").center(10))
```

42. **Ljust**  
```python
print(input("String: ").ljust(10))
```

43. **Rjust**  
```python
print(input("String: ").rjust(10))
```

44. **Partition**  
```python
print(input("String: ").partition(input("Sep: ")))
```

45. **Split (default)**  
```python
print(input("String: ").split())
```

46. **Join with Dash**  
```python
print("-".join(input("Enter words separated by spaces: ").split()))
```

47. **Replace**  
```python
print(input("String: ").replace(input("Old: "), input("New: ")))
```

48. **Count Vowels**  
```python
print(sum(ch in "aeiouAEIOU" for ch in input("String: ")))
```

49. **Count Consonants**  
```python
print(sum(ch.isalpha() and ch not in "aeiouAEIOU" for ch in input("String: ")))
```

50. **Reverse**  
```python
print(input("String: ")[::-1])
```
