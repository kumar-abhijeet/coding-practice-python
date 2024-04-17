## Python has 12 primary built-in data types:

| Category | Name | Description | 
| --- | --- | --- |
| None | `None` | The null object |
| Numeric | `int` | Integer |
|  | `float` | Floating point number |
|  | `complex` | Complex number |
|  | `bool` | Boolean (True, False) |
| Sequences | `str` | String of characters |
|  | `list` | List of arbitrary objects |
|  | `tuple` | Group of arbitrary items |
|  | `range` | Creates a range of integers |
| Mapping | `dict` | Dictionary of key-value pairs |
| Set | `set` | Mutable, unordered collection of unique items |
|  | `frozenset` | Immutable set |

Also, `decimal` and `fractions` module can be used for certain use cases:

* `import decimal`
* `import fractions`

---

## Modules for Data Structures and Algorithms 

#### Collections

`from collections import abc`

| Datatype or operation | Description | 
| --- | --- | 
| `namedtuple()` | Creates tuple subclasses with named fields | 
| `deque` | Lists with fast appends and pops either end | 
| `ChainMap` | Dictionary like class to create a signle view of multiple mappings | 
| `Counter` | Dictionary subclass for counting hasable objects | 
| `OrderedDict` | Dictionary subclass that remembers the entry order | 
| `defaultDict` | Dictionary subclass that calls a function to supply missing values | 
| `UserDict`, `UserList`, `UserString` | These 3 data types are simply wrappers for their underlyuing base classes. Their use has largely been replaced by the ability to subclass their respective base classes directly. Can be used to access the underlying obect as an attribute | 

#### Arrays

`import array`

It defines a datatype `array` that is similar to the `list` datatype except for the constraint that their contents must be of a single type of the underlying representation

---

### Conditional Statements: if, elif, else

```
x = -15

if x==0:
  print(x, "is zero)
elif x>0:
  print(x, "is positive)
elif x<0:
  print(x, "is negative)
else:
  print(x, "is unlike anything I've ever seen")

```

---

### for loops

```
for N in [2,3,5,7]:
  print(N, end = ' ') #print all in the same line

# output: 2 3 5 7
```

#### break and continue: Fine-tuning your loops

* break - exit loop (breaks out of the loop entirely)
* continue - skip iteration (skips remainder of current loop, goes to next iteration)
* pass - do nothing (acts as a placeholder, often when you begin coding)

### Loops with an `else` block (like a nobreak statement)

 `else` block is executed only if the loop ends naturally, without encountering a `break` statement

 ```
# non-optimized algo of the Sieve of Eratosthenes (for finding prime numbers)

L = []
nmax = 30

for n in range(2, nmax):
  for factor in L:
    if n % factor == 0:
      break
  else: # no break)
      L.append(n)
print(L)

# output : [2,3,5,7,11,13,17,19,23,29]
```

---

### while loops

```
i = 0
while i < 10:
  print(i, end = ' ')
  i += 1

# output: 0 1 2 3 4 5 6 7 8 9
```

---




















