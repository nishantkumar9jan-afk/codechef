# ELECTN - Rating 594

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-01T16:52:45.591Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    // Fast I/O
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int t;
    cin >> t;
    while (t--) {
        int x, a, b;
        cin >> x >> a >> b;

        // Calculate total points: each easy problem is 1 point, each hard is 2 points
        int total_points = a + (2 * b);

        // Check if Chef qualifies
        if (total_points >= x) {
            cout << "Qualify\n";
        } else {
            cout << "NotQualify\n";
        }
    }

    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/ELECTN)