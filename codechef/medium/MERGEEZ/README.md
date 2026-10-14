# MERGEEZ

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

### Merging (Easy)

Define $merge(A, B)$ as the array $C$ formed by the following process:

- Initialize $i = 0, j = 0, C = []$ (empty array)
- While both $i < |A|, j < |B|$ holds, do the following: if $A_i < B_j$, append $A_i$ to $C$ and increment $i$ by $1$. Else, append $B_j$ to $C$ and increment $j$ by $1$.
- While $i < |A|$, append $A_i$ to $C$ and increment $i$ by $1$.
- While $j < |B|$, append $B_j$ to $C$ and increment $j$ by $1$.

For example, it can be shown that $merge([2, 3], [1, 4]) = [1, 2, 3, 4]$, and $merge([3, 2], [4, 1]) = [3, 2, 4, 1]$.

You are given a permutation $P$ of the integers $[1, N].$

For each $i = 0, 1, 2, \ldots, N$, count how many pairs of arrays $A$ and $B$ exist such that $merge(A, B) = P$ and $|A| = i$. Since the answers may be large, output them modulo $998244353$.

### Input Format
- The first line of input will contain a single integer $T$, denoting the number of test cases.
- Each test case consists of multiple lines of input. The first line contains a single integer $N$. The second line contains $N$ integers - $P_1, P_2, \ldots, P_N$.
### Output Format

For each test case, output on a new line $N + 1$ integers - the number of pairs of arrays $A$ and $B$ such that $|A| = i$ for each $i = 0, 1, \ldots, N$ modulo $998244353$.

### Constraints
- $1 \le T \le 100$
- $1 \le N \le 5000$
- $1 \le P_i \le N$
- $P_i \ne P_j$ for all $i \ne j$
- The sum of $N$ over all test cases does not exceed $5000$.
### Sample 1:
Input
Output

```
4
4
1 2 3 4
4
3 2 4 1
1
1
7
2 4 3 6 5 1 7

```

```
1 4 6 4 1
1 0 2 0 1
1 1
1 2 2 3 3 2 2 1
```

### Explanation:

 **Test Case 1:**  Every sorted subset of $P$ works as $A$, and its complement as $B$. This is because the merge (as defined) of $2$ sorted arrays will always be sorted.

 **Test Case 2:**  The possibilities are:

- $A = [], B = [3, 2, 4, 1]$
- $A = [3, 2], B = [4, 1]$
- $A = [4, 1], B = [3, 2]$
- $A = [3, 2, 4, 1], B = []$

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-14T16:09:49.900Z  

```c_cpp

#include <bits/stdc++.h>
using namespace std;

const int MOD = 998244353;

void solve() {
    int n;
    cin >> n;
    vector<int> p(n);
    for (int i = 0; i < n; i++) {
        cin >> p[i];
    }
    
   
    
    vector<long long> ans(n + 1, 0);
    // Base case for single element
    dp[0] = 1; // means last was in B or empty? Let's track (i, last_array)
    
    // Let's use a clear DP state: dp[i][0] -> length i for A, last added to A
    // dp[i][1] -> length i for A, last added to B
    vector<long long> dpA(n + 1, 0), dpB(n + 1, 0);
    if (n > 0) {
        dpA[1] = 1; // p[0] can start A
        dpB[0] = 1; // or start B (so length of A is 0)
    }
    
    for (int k = 1; k < n; k++) {
        vector<long long> ndpA(n + 1, 0), ndpB(n + 1, 0);
        bool greater = (p[k] > p[k - 1]);
        
        for (int i = 0; i <= k; i++) {
            // From A last
            if (dpA[i]) {
                // Extend A
                ndpA[i + 1] = (ndpA[i + 1] + dpA[i]) % MOD;
                // Extend B (switch to B)
                if (greater) {
                    ndpB[i] = (ndpB[i] + dpA[i]) % MOD;
                } else {
                    // If p[k] < p[k-1], switching is invalid if we follow strict merge where smaller comes first,
                    // wait! If p[k] < p[k-1], can it switch? 
                    // If we switch to B, B's current element would be p[k], and A's last was p[k-1]. 
                    // Since p[k] < p[k-1], the merge algorithm would have picked p[k] from B *before* p[k-1] from A!
                    // Thus, if p[k] < p[k-1], we CANNOT have last been in A and now switch to B.
                    // So switching is only allowed when p[k] > p[k-1].
                }
            }
            // From B last
            if (dpB[i]) {
                // Extend B
                ndpB[i] = (ndpB[i] + dpB[i]) % MOD;
                // Extend A (switch to A)
                if (greater) {
                    ndpA[i + 1] = (ndpA[i + 1] + dpB[i]) % MOD;
                }
            }
        }
        dpA = move(ndpA);
        dpB = move(ndpB);
    }
    
    for (int i = 0; i <= n; i++) {
        ans[i] = (dpA[i] + dpB[i]) % MOD;
    }
    
    for (int i = 0; i <= n; i++) {
        cout << ans[i] << (i == n ? "" : " ");
    }
    cout << "\n";
}

int main() {
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    int t;
    cin >> t;
    while (t--) {
        solve();
    }
    return 0;
}

```

---

[View on CodeChef](https://www.codechef.com/problems/MERGEEZ)