# MONOPOLY2 - Rating 578

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

### Monopoly

There are $4$ companies in the markets of Chefland, $A$, $B$, $C$, and $D$. $\\$ This year,

- Company $A$ made a profit of $P$ lakh rupees,
- Company $B$ made a profit of $Q$ lakh rupees,
- Company $C$ made a profit of $R$ lakh rupees,
- Company $D$ made a profit of $S$ lakh rupees.

There is said to be a  **monopoly**  in the market if the profit made by one company is  **strictly greater than**  the sum of profits made by all other companies. $\\$ Determine if there is a monopoly in the market or not.

### Input Format
- The first line of input will contain a single integer $T$, denoting the number of test cases.
- The first line and only line of each test case contains four space-separated integers $P$, $Q$, $R$ and $S$ — the profits made by companies $A$, $B$, $C$ and $D$ respectively.
### Output Format

For each test case, output `YES` if there is a monopoly in the market. Otherwise, output `NO`.

You may print each character of `YES` and `NO` in uppercase or lowercase (for example, `yes`, `yEs`, `Yes` will be considered identical).

### Constraints
- $1 \leq T \leq 5000$
- $1 \leq P, Q, R, S \leq 100$
### Sample 1:
Input
Output

```
4
1 1 1 10
30 20 6 4
100 90 3 4
14 15 16 17

```

```
YES
NO
YES
NO

```

### Explanation:

 **Test Case 1:**  Here, company $D$'s profit ($10$) is greater than the sum of profits of all other companies ($1 + 1 + 1 = 3$).

 **Test Case 2:**  Here, no company's profit is  **strictly**  greater than the sum of profits of all other companies.

 **Test Case 3:**  Here, company $A$'s profit ($100$) is greater than the sum of profits of all other companies ($90 + 3 + 4 = 97$).

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-26T18:08:43.885Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

void solve() {
    int p, q, r, s;
    cin >> p >> q >> r >> s;
    
    int total_sum = p + q + r + s;
    int max_profit = max({p, q, r, s});
    
    if (2 * max_profit > total_sum) {
        cout << "YES\n";
    } else {
        cout << "NO\n";
    }
}

int main() {
    // Fast I/O
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

[View on CodeChef](https://www.codechef.com/problems/MONOPOLY2)