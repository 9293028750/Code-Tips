**Binary Search**
```
def binarySearch(self, A):
    lo, hi = 0, len(A) - 1
    while lo < hi:
        mi = (lo + hi) / 2
        if A[mi] < A[mi + 1]:
            lo = mi + 1
        else:
            hi = mi
    return lo
```

**swap using two indexes**
```
def reverseOnlyLetters(self, S):
    i = 0
    j = len(S) - 1
    S = list(S)
    while i < j:
        if not S[i].isalpha():
            i += 1
            continue
        if not S[j].isalpha():
            j -= 1
            continue
        S[i], S[j] = S[j], S[i]
        i += 1
        j -= 1
    return "".join(S)
```

**Binary Trees**

**Transpose Matrix**
zip(*matrix)

**yield**
```
def leafSimilar(self, root1, root2):
        def dfs(node):
            if node:
                if not node.left and not node.right:
                    yield node.val
                yield from dfs(node.left)
                yield from dfs(node.right)

        return list(dfs(root1)) == list(dfs(root2))
```

**find single Number**
```
def singleNumber(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        output = 0
        for val in nums:
            output ^= val
            
        return output
```

**deep first search**
Simply convert the employees array/list into a map for easy lookup and then do a DFS traversal from the "root" employee node.
```
def getImportance(self, employees, id):
        """
        :type employees: Employee
        :type id: int
        :rtype: int
        """
        emps = {employee.id: employee for employee in employees}
        dfs = lambda id: sum([dfs(sub_id) for sub_id in emps[id].subordinates]) + emps[id].importance
        return dfs(id) 
```

**Bit Operators**
1 byte = 8 bit
```
N = 0011 1100


0 ^ N = N
N ^ N = 0
N ^ N ^ M = M


string
list
dict
bit
array

tree
data structure implement
regular express