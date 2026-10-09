# BATH - Rating 641

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-09T17:18:59.753Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

void solve() {
    int n, x;
    cin >> n >> x;
    
    cout << min(x, n - x) << "\n";
}

int main() {
   
    
    int t;
    cin >> t;
    while (t--) {
        solve();
    }
    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/BATH)