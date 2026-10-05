# MAXTASTE - Rating 622

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-05T16:39:27.873Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
 
    int t;
    cin >> t;
    while(t--) {
        int a, b, c;
        cin >> a >> b >> c;
       
        cout << max({a, b, c}) << "\n";
    }
    
    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/MAXTASTE)