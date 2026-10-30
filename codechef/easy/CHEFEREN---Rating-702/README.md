# CHEFEREN - Rating 702

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-30T17:05:53.747Z  

```c_cpp
#include <iostream>
#include <algorithm>

using namespace std;

int main() {
    int t;
    cin >> t;
    while (t--) {
        int s, x, y, z;
        cin >> s >> x >> y >> z;
        
        // Calculate current free memory
        int free_memory = s - (x + y);
        
        // If free memory is already enough, 0 apps to delete
        if (free_memory >= z) {
            cout << 0 << "\n";
        }
        // If deleting the larger app gives enough memory, 1 app to delete
        else if (free_memory + max(x, y) >= z) {
            cout << 1 << "\n";
        }
        // Otherwise, we must delete both apps, 2 apps to delete
        else {
            cout << 2 << "\n";
        }
    }
    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/CHEFEREN)