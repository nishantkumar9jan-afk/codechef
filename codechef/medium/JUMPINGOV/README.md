# JUMPINGOV

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

### Jumping Over

You are given a permutation $P$ of the integer $[1, N]$ and can perform the following operation:

- Choose an index $i$, and move it to the front or the back of the permutation (appropriately shifting the other indices).
- The cost of moving it to the front is $(i - 1)$, and the cost of moving it to the back is $(N - i)$, i.e. the cost is simply the number of elements it jumps over.

Find the minimum total cost of operations needed to sort the permutation $P$.

### Input Format
- The first line of input will contain a single integer $T$, denoting the number of test cases.
- Each test case consists of multiple lines of input. The first line contains a single integer $N$. The second line contains $N$ integers - $P_1, P_2, \ldots, P_N$.
### Output Format

For each test case, output on a new line the minimum cost.

### Constraints
- $1 \le T \le 10^4$
- $2 \le N \le 2 \cdot 10^5$
- $1 \le P_i \le N$
- $P_i \ne P_j$ for all $i \ne j$
- The sum of $N$ over all test cases does not exceed $2 \cdot 10^5$
### Sample 1:
Input
Output

```
4
2
2 1
4
4 2 3 1
3
1 2 3
6
2 4 1 6 5 3

```

```
1
5
0
10
```

### Explanation:

 **Test Case 1:**  You can choose the element $2$ at index $1$ and move it back, jumping over $1$ element. Then, the permutation is sorted, so the cost is only $1$.

 **Test Case 2:**  Move the value $4$ to the back, cost $3$, permutation is $[2, 3, 1, 4]$; and then move the value $1$ to the front, cost $2$. The total cost is $5$.

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-16T16:20:17.828Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
	// your code goes here

}

```

---

[View on CodeChef](https://www.codechef.com/problems/JUMPINGOV)