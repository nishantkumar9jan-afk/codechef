# DIFFGCD

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

### Difference is GCD

You are given an integer $N$. Count the number of pairs $(X, Y)$ such that:

- $1 \le X < Y \le N$
- $gcd(X, Y) = |X - Y|$

where $gcd(A, B)$ denotes the greatest common divisor of both $A$ and $B$.

### Input Format
- The first line of input will contain a single integer $T$, denoting the number of test cases.
- The first and only line of each test case contains a single integer $N$.
### Output Format

For each test case, output the number of pairs $(X, Y)$ satisfying the conditions.

### Constraints
- $1 \le T \le 100$
- $2 \le N \le 10^9$
### Sample 1:
Input
Output

```
4
2
3
4
10

```

```
1
2
4
17
```

### Explanation:

 **Test Case 1:**  $(1, 2)$ is the only pair.

 **Test Case 2:**  $(1, 2)$ and $(2, 3)$ are valid pairs.

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-14T16:06:19.926Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

void solve() {
    long long n;
    cin >> n;
    
    // We want to count pairs (X, Y) such that 1 <= X < Y <= N and gcd(X, Y) = Y - X.
    // Let g = Y - X. Then Y = X + g.
    // The condition gcd(X, X + g) = g is equivalent to gcd(X, g) = g,
    // which means g must divide X.
    // Thus, X must be a multiple of g: X = k * g for some integer k >= 1.
    // Since Y = X + g <= N, we have k * g + g <= N => (k + 1) * g <= N => k <= N / g - 1.
    // Since k >= 1, the number of valid values of k for a fixed g is max(0LL, N / g - 1).
    // Or equivalently, X can be g, 2g, 3g, ..., such that X + g <= N, which is (N - g) / g.
    
    long long total_pairs = 0;
    for (long long g = 1; g * g < n; g++) {
        total_pairs += (n - g) / g;
    }
    
    cout << total_pairs << "\n";
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

[View on CodeChef](https://www.codechef.com/problems/DIFFGCD)