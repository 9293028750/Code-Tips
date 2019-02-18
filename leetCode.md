**动态规划**

题型：
    记数型动态规划
    最值型动态规划
    存在型动态规划


组成部分：
    确定状态
        最后一步
        分解子问题 
        定状态
    * 转移方程  Transition Function
    初始条件和边界情况
    计算顺序

类型：
    坐标型动态规划 （20%）
    序列型动态规划 （20%）
    划分型动态规划 （20%）
    区间型动态规划 （15%）
    背包型动态规划 （10%）
    最长序列型动态规划 （5%）
    博弈型动态规划 （5%）
    综合型动态规划 （5%）


===============================

**贪心算法**

定义：
贪心算法（又称贪婪算法）是指，在对问题求解时，总是做出在当前看来是最好的选择。 也就是说，不从整体最优上加以考虑，他所做出的是在某种意义上的局部最优解。 

难点：
通常贪心算法的代码会非常短而且思路也非常的简单，但贪心算法真正的难点在于确定我们当前的问题确实可以使用贪心算法。

思路：
贪心算法通常和排序是分不开的，如果题目给出数组没有排序，我们就需要自己进行排序。



===============================

**Binary Search** (logn)




===============================

**Two Point**

同向双指针

快慢双指针

反向双指针

Partition



===============================

**BFS**
图的遍历 (Traversal in Graph)
    层级遍历 (Level Order Traversal)
    由点及面 (Connected Component)
    拓扑排序 (Topological Sorting)

最短路径 (Shortest Path in Simple Graph)

非递归的方式找到所有方案 (Iteration solution for all possible results)


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


N>>=1   <=>   N = N // 2
N&1 <=> N % 2


string
list
dict
bit
array

tree
data structure implement
regular express