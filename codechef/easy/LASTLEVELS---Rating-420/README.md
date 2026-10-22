# LASTLEVELS - Rating 420

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-22T15:02:29.731Z  

```c_cpp
#include <iostream>
#include <cmath>

using namespace std;

int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        // sqrt() returns a double, casting to int truncates the decimal part (rounds down)
        int ans = sqrt(n);
        cout << ans << "\n";
    }
    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/LASTLEVELS)