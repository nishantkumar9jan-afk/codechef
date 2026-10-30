# MINCOINS - Rating 706

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-10-30T17:06:12.846Z  

```c_cpp
#include <iostream>

using namespace std;

int main() {
    // Fast I/O
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int t;
    cin >> t;
    while (t--) {
        int n, a, b;
        cin >> n >> a >> b;
        
        // n / 2 gives the number of even-indexed episodes
        // n - (n / 2) gives the number of odd-indexed episodes
        int even_episodes = n / 2;
        int odd_episodes = n - even_episodes;
        
        int total_duration = (even_episodes * a) + (odd_episodes * b);
        
        cout << total_duration << "\n";
    }

    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/MINCOINS)