# CHEFBOTTLE - Rating 660

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-15T15:44:25.185Z  

```c_cpp
#include <iostream>
#include <string>

using namespace std;

void solve() {
    int n;
    cin >> n;
    string s;
    cin >> s;
    
    for (int i = 0; i < n; i++) {
        if (s[i] == 'A') {
            cout << 'T';
        } else if (s[i] == 'T') {
            cout << 'A';
        } else if (s[i] == 'C') {
            cout << 'G';
        } else if (s[i] == 'G') {
            cout << 'C';
        }
    }
    cout << "\n";
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

[View on CodeChef](https://www.codechef.com/problems/CHEFBOTTLE)