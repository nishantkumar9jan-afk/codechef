# FLOORS - Rating 716

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-11-04T10:13:56.950Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    // Fast I/O
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int T;
    cin >> T;
    while (T--) {
        int X, Y, D;
        cin >> X >> Y >> D;

        // Check if the absolute difference is less than or equal to D
        if (abs(X - Y) <= D) {
            cout << "YES\n";
        } else {
            cout << "NO\n";
        }
    }

    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/FLOORS)