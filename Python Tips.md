**Generator Expression**
```
gen = (x for x in xyz if x not in a)
for x in gen:
    print x
```
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
> Map applies a function to all the items in an input_list. 
```
items = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x**2, items))
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

** create index for using dictionnary**
** all | set | enumerate**
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

