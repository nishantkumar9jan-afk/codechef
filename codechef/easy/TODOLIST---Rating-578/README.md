# TODOLIST - Rating 578

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-26T18:08:49.184Z  

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

[View on CodeChef](https://www.codechef.com/problems/TODOLIST)