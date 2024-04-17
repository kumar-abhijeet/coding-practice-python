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

##### break and continue: Fine-tuning your loops

* break - exit loop (breaks out of the loop entirely)
* continue - skip iteration (skips remainder of current loop, goes to next iteration)
* pass - do nothing (acts as a placeholder, often when you begin coding)

##### Loops with an `else` block (like a nobreak statement)

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

### Defining Functions

Defining Functions

```
def fibonacci(N):

  L = []
  a, b = 0, 1

  while len(L) < N:
    a, b = b, a+b
    L.append(a)

  return L
```

Using Functions

```
fibonacci(10)

[1,1,2,3,5,8,13,21,34,55]
```

Functions can return any Python object, simple or compound 

Multiple Return Values (put in a tuple)

```
# define the function
def real_img_conj(val):
  return val.real, val.imag, val.conjugate()

# use the function
r, i, c = real_img_conj(3 + 4j)
print(r, i, c)

#output: 3.0 4.0 (3-4j)
```

Default Argument values in Function

```
#define the function with default arg. values
def fibonacci(N, a=0, b=1):
  L = []

  while len(L) < N:
    a, b = b, a+b
    L.append(a)

  return L

# use the function
fibonacci(10)
# output: [1,1,2,3,5,8,13,21,34,55]

fibonacci(10,0,2)
# output: [2,2,4,6,10,16,26,42,68,110]

fibonacci(10,b=3,a=1)
# output: [3,4,7,11,18,29,47,76,123,199]
```


*args and **kwargs: Flexible Arguments

































