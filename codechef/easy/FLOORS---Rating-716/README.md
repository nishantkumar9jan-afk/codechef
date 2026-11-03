# FLOORS - Rating 716

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-11-03T14:06:38.684Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    
    int T;
    cin >> T;
    while (T--) {
        int X, Y, D;
        cin >> X >> Y >> D;

        
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