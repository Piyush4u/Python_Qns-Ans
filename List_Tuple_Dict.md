## LIST
### Q1
```python
a = [1, 2, 3]
b = a
b.append(4)
print(a)
```
**Output**
```
[1, 2, 3, 4]
```

### Q2
```python
a = [1, 2, 3]
b = a.copy()
b.append(4)
print(a)
```
**Output**
```
[1, 2, 3]
```

### Q3
```python
lst = [10, 20, 30, 40]
print(lst[-1])
```
**Output**
```
40
```

### Q4
```python
lst = [1, 2, 3]
print(lst * 2)
```
**Output**
```
[1, 2, 3, 1, 2, 3]
```

### Q5
```python
lst = [1, 2, 3]
lst.append([4, 5])
print(len(lst))
```
**Output**
```
4
```

### Q6
```python
lst = [1, 2, 3]
lst.extend([4, 5])
print(len(lst))
```
**Output**
```
5
```

### Q7
```python
lst = [10, 20, 30]
print(lst.pop())
```
**Output**
```
30
```

### Q8
```python
lst = [1, 2, 3]
lst.remove(2)
print(lst)
```
**Output**
```
[1, 3]
```

### Q9
```python
lst = [1, 2, 3]
print(lst.index(3))
```
**Output**
```
2
```

### Q10
```python
lst = [1, 2, 3]
lst.clear()
print(lst)
```
**Output**
```
[]
```

---

## TUPLE

### Q11
```python
t = (10)
print(type(t))
```
**Output**
```
<class 'int'>
```

### Q12
```python
t = (10,)
print(type(t))
```
**Output**
```
<class 'tuple'>
```

### Q13
```python
t = (1, 2, 3)
t = t + (4, 5)
print(t)
```
**Output**
```
(1, 2, 3, 4, 5)
```

### Q14
```python
t = (1, 2, 3)
print(t * 2)
```
**Output**
```
(1, 2, 3, 1, 2, 3)
```

### Q15
```python
t = (10, 20, 30)
print(t[-2])
```
**Output**
```
20
```

### Q16
```python
t = (1, (2, 3))
print(t[1][0])
```
**Output**
```
2
```

### Q17
```python
t = (1, 2, 3)
print(len(t))
```
**Output**
```
3
```

### Q18
```python
t = (5, 5, 5)
print(t.count(5))
```
**Output**
```
3
```

### Q19
```python
t = (1, 2, 3)
print(4 in t)
```
**Output**
```
False
```

### Q20
```python
t = (1, 2, 3)
del t
print(t)
```
**Output**
```
NameError
```

---

## DICTIONARY

### Q21
```python
d = {"a": 1, "b": 2}
print(d["a"])
```
**Output**
```
1
```

### Q22
```python
d = {"a": 1}
d["a"] = 5
print(d)
```
**Output**
```
{'a': 5}
```

### Q23
```python
d = {}
d[1] = "one"
d[1] = "ONE"
print(d)
```
**Output**
```
{1: 'ONE'}
```

### Q24
```python
d = {"a": 1, "b": 2}
print(len(d))
```
**Output**
```
2
```

### Q25
```python
d = {"x": 10}
print(d.get("y"))
```
**Output**
```
None
```

### Q26
```python
d = {"x": 10}
print(d.get("x", 0))
```
**Output**
```
10
```

### Q27
```python
d = {"a": 1, "b": 2}
print(list(d.keys()))
```
**Output**
```
['a', 'b']
```

### Q28
```python
d = {"a": 1, "b": 2}
print(list(d.values()))
```
**Output**
```
[1, 2]
```

### Q29
```python
d = {"a": 1, "a": 2}
print(d)
```
**Output**
```
{'a': 2}
```

### Q30
```python
d = {1: "one", 2: "two"}
print(1 in d)
```
**Output**
```
True
```
