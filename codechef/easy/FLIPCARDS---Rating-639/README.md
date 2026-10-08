# FLIPCARDS - Rating 639

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-08T16:31:25.472Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

void solve() {
    int x, y;
    cin >> x >> y;
    // The time taken is the absolute difference between their positions
    cout << abs(x - y) << "\n";
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

[View on CodeChef](https://www.codechef.com/problems/FLIPCARDS)