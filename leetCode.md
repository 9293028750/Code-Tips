**考察频率，学习难度**

   算法      考察评率   难度  掌握需要的题量  性价比
宽度优先搜索     高      中      5~10        极高
二分法          高      中      10~20       高
双指针          高      中      10~20       高
哈希表          高      中      10~30       高
二叉树，链表     高      低      30~50       高

深度优先搜索     高      高       20~40      中
字符串，模拟法    高      低      20~50       中
堆(优先队列)     低      中       5~10       中
树状数组         低      中       2~3        中

字典树          中      低      2~5         高
并查集          低      低      2~5         高
动态规划        中      高      40~60       低



**刷题的三个维度**：
    1. 算法知晓能力
    2. Bug Free 能力
    3. 题量

    很多人只关心第三个维度，但这个维度是最弱的维度。

**代码质量**
    最容易出卖你的，就是你的Coding Style。工程师的代码长什么样比脸长什么样更重要。
    代码质量很重要。
    好的代码质量包括：
        Bug Free
        好的代码风格
            包括变量名命名规范有意义
            加注解
            合理的使用空行
            善用空行
        容易让人读懂的逻辑。
            要把复杂的事情用简单的方，别把简单的事情写复杂了。
        没有冗余代码
        有边界检测和异常处理

**评分体系**    
    Strong Hire
        使用O(n)或者O(nlogn)的算法实现出来，
        并且代码质量合格，
        无Bug或者有很小的bug，但是自己发现并解决，无需太多的提示。
    Hire
        能够分别使用枚举法和动态规划实现时间复杂度O(n^2)的算法。
        并且代码质量优秀，
        无Bug，
        无重复代码，
        无需面试官给提示。
    Weak Hire
        只用了其中一种O(n^2)的算法实现出来，
        代码质量还不错，
        可以有一些小Bug，面试官可以给一些小提示。
    No Hire
        只想出一种O(n^2)的算法，
        但是Bug太多，
        或者需要很多提示


**总决式**    
    1.别做难题
        不要花时间攻关难题，多做Medium难度的题
    2.是面试不是考试
        和面试官愉快的交流，一起合作解决面试的问题（沟通能力）。
    3.理解而不是单纯的背诵
        主要学习的是思维方式和分析技巧，而不是某道题的解法
    4.反复练习
        把时间花在如何做到Bug Free和提高编程速度上
        代码超过50行的题，可以反复写几遍
        **天下武功为快不破**



**心态**
    面试是5分运气，5分实力。
    带着尽人事知天命的心态去准备面试，才能更从容的应对。


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

===============================
二叉树
    1. 求值，求路径类二叉树
    2. 结构变化类二叉树
    3. 二叉查找树类问题
        非递归(Iteration)版本的中序遍历(Inoder Traversal)





搜索 Search
    宽度优先遍历 BFS

    深度优先遍历 DFS = 回溯法 Backtracking
        遍历法 Traversal
            递归 Recursion

            迭代 Iteration = 非递归 None-Recursion
        分治法 Divide&Conquer





===============================
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