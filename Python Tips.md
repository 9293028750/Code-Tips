**Improve**
collections.Counter()
Tree (Using Recursion)
Binary Search
**String**
```
str.count(sub, start= 0,end=len(string))
returns the number of occurrences of substring sub in the range [start, end].

str.find(sub[, start[, end]] )
returns the index of first occurrence of the substring (if found). If not found, it returns -1.
```
**List**
```
extend()
The extend() extends the list by adding all items of a list (passed as an argument) to the end.

pop()
The pop() method removes and returns the element at the given index (passed as an argument) from the list.
```
**collections**
```
collections.Counter()
```
abcdefghijklmnopqrstuvwxyz
**Built-in**
```
chr(i) 
Return the string representing a character whose Unicode code point is the integer i.
chr(97) returns the string 'a', while chr(8364) returns the string '€'

ord(c)
Given a string representing one Unicode character, return an integer representing the Unicode code point of that character. 

```

**Generator Expression**
Generators are iterators, but you can only iterate over them once. It’s because they do not store all the values in memory.
```
gen = (x*x for x in range(3))
for x in gen:
    print x
```

**yiled**
Yield is a keyword that is used like return, except the function will return a generator.

To master yield, you must understand that when you call the function, the code you have written in the function body does not run. The function only returns the generator object, this is a bit tricky

**yield from**
The short explanation is that it enables you to easily refactor a generator by splitting it up into multiple generators.

**Enumerate**
>Enumerate() method adds a counter to an iterable and returns it in a form of >enumerate object. 
```
my_list = ['apple', 'banana', 'grapes', 'pear']
for c, value in enumerate(my_list, 1):
    print(c, value)

# Output:
# 1 apple
# 2 banana
# 3 grapes
# 4 pear
```

**Zip**
>The purpose of zip() is to map the similar index of multiple containers so that >they can be used just using as single entity.
```
# initializing lists 
name = [ "Manjeet", "Nikhil", "Shambhavi", "Astha" ] 
roll_no = [ 4, 1, 3, 2 ] 
marks = [ 40, 50, 60, 70 ] 

# using zip() to map values 
mapped = zip(name, roll_no, marks) 

# converting values to print as set 
mapped = set(mapped) 

# printing resultant values 
print ("The zipped result is : ",end="") 
print (mapped) 

```
**map()**
> The map() function applies a given function to each item of an iterable (list, tuple etc.) and returns a list of the results.
map(function, iterable)
```
items = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, items))


def numJewelsInStones(self, J, S):
    return sum(map(J.count, S))
```

**filter()**
> filter creates a list of elements for which a function returns true. . 
```
number_list = range(-5, 5)
less_than_zero = list(filter(lambda x: x < 0, number_list))
print(less_than_zero)

# Output: [-5, -4, -3, -2, -1]
```

**reduce()**
> Reduce is a really useful function for performing some computation on a list and > returning the result. It applies a rolling computation to sequential pairs of 
> values in a list
```
items = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, items))
```

**create index for using dictionnary**
**all | set | enumerate**
```
test1_attrs = ['A', 'B', 'C', 'D']
test2_attrs = ['B', 'D', 'E']

test1_tuples = [
    ['A', 1, 'A', 'a'],
    ['B', 2, 'Y', 'a'],
    ['Y', 4, 'B', 'b'],
    ['A', 1, 'Y', 'a'],
    ['S', 2, 'B', 'b']]

test2_tuples = [
    [1, 'a', 'A'],
    [3, 'a', 'B'],
    [1, 'a', 'Y'],
    [2, 'b', 'S'],
    [3, 'b', 'E']]

test1_columns = set(test1_attrs)
test2_columns = set(test2_attrs)

test1_map = {k:i for i,k in enumerate(test1_attrs)}
test2_map = {k:i for i,k in enumerate(test2_attrs)}

join_on = test1_columns & test2_columns
diff = test1_columns - join_on

def match(row1,row2):
    return all(row1[test1_map[rn]] == row2[test2_map[rn]] for rn in join_on)

result = []
for test1_row in test1_tuples:
    for test2_row in test2_tuples:
        if match(test1_row, test2_row):
            row = test1_row[:]
            for rn in diff:
                row.append(rn)
            result.append(row)           
print(result)
```

**generator**
> Generators are best for calculating large sets of results (particularly 
> calculations involving loops themselves) where you don't want to allocate the 
> memory for all results at the same time.
```
# generator version
def fibon(n):
    a = b = 1
    for i in range(n):
        yield a
        a, b = b, a + b

for x in fibon(1000000):
    print(x)
```

**zip**
```
dishes = ["pizza", "sauerkraut", "paella", "hamburger"]
countries = ["Italy", "Germany", "Spain", "USA"]
dict(zip(countries, dishes))
{'USA': 'hamburger', 'Germany': 'sauerkraut', 'Spain': 'paella', 'Italy': 'pizza'}

list(zip(countries, dishes))
[('Italy', 'pizza'), ('Germany', 'sauerkraut'), ('Spain', 'paella'), ('USA', 'hamburger')]
```

**Bit Operators**
1 byte = 8 bit
```
a = 0011 1100

b = 0000 1101

-----------------

a&b = 0000 1100

a|b = 0011 1101

a^b = 0011 0001

~a  = 1100 0011

a << 2 = 1111 0000

a >> 2  =  0000 1111


0 ^ N = N
N ^ N = 0


```
**[::]**
```
L = range(10)
L[::2]
[0, 2, 4, 6, 8]

L[::-1]
[9, 8, 7, 6, 5, 4, 3, 2, 1, 0]


```

**Set operator**
x1.union(x2[, x3 ...])
x1 | x2 [| x3 ...]

x1.intersection(x2[, x3 ...])
x1 & x2 [& x3 ...]

x1.difference(x2[, x3 ...])
x1 - x2 [- x3 ...]

x1.symmetric_difference(x2)
x1 ^ x2 [^ x3 ...]

x1.isdisjoint(x2)

x1.issubset(x2)
x1 <= x2

x1 < x2

x1.issuperset(x2)
x1 >= x2

x1 > x2

x1.update(x2[, x3 ...])
x1 |= x2 [| x3 ...]

x1.intersection_update(x2[, x3 ...])
x1 &= x2 [& x3 ...]

x1.difference_update(x2[, x3 ...])
x1 -= x2 [| x3 ...]

x1.symmetric_difference_update(x2)
x1 ^= x2