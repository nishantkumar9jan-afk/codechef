# DBLDROP

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

### Double and Drop (Easy)

You are given an array $A$ of $N$ positive integers.

You may perform the following operation  **at most once** :

- Choose an index $i$ ($1 \le i \le N$) and set $A_i := 2 \cdot A_i$.

After that, let $f(A)$ be the maximum possible value of $\text{sum}(A) - \max(A)$, that is, the sum of all its elements except one copy of the largest one.

Given an array of $N$ elements, find $f(A)$.

### Input Format
- The first line of input will contain a single integer $T$, denoting the number of test cases.
- Each test case consists of two lines of input. The first line of each test case contains a single integer $N$ — the length of the array. The second line contains $N$ space-separated integers $A_1, A_2, \ldots, A_N$.
### Output Format

For each test case, output on a new line the maximum possible score $f(A)$.

### Constraints
- $1 \leq T \leq 1000$
- $2 \leq N \leq 5000$
- $1 \leq A_i \leq 10^9$
- The sum of $N$ over all test cases does not exceed $5000$.
### Sample 1:
Input
Output

```
4
3
1 2 3
2
5 5
3
1 6 10
5
7 3 9 2 9

```

```
4
5
11
24

```

### Explanation:

 **Test case $1$:**  Doubling $A_1$ gives $[2, 2, 3]$, with score $7 - 3 = 4$. Doubling $A_2$ gives $[1, 4, 3]$, with score $8 - 4 = 4$ as well. No choice does better.

 **Test case $2$:**  Without the operation, the score is $10 - 5 = 5$. Doubling either element gives score $15 - 10 = 5$.

 **Test case $3$:**  Doubling $A_2$ gives $[1, 12, 10]$. The maximum changes, but the score is $23 - 12 = 11$, which is optimal.

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-11-25T16:02:37.121Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int T;
    if (!(cin >> T)) return 0;

    while (T--) {
        int N;
        cin >> N;

        vector<long long> A(N);
        long long total_sum = 0;
        long long max_val = 0;

        for (int i = 0; i < N; ++i) {
            cin >> A[i];
            total_sum += A[i];
            if (A[i] > max_val) {
                max_val = A[i];
            }
        }

        // Case 1: Perform 0 operations (no doubling)
        long long ans = total_sum - max_val;

        // Case 2: Double one element A[i] -> 2 * A[i]
        for (int i = 0; i < N; ++i) {
            long long new_total = total_sum + A[i];
            long long new_max = max(max_val, 2 * A[i]);
            ans = max(ans, new_total - new_max);
        }

        cout << ans << '\n';
    }

    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/DBLDROP)