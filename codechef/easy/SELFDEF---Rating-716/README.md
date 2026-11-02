# SELFDEF - Rating 716

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

### Self Defence Training

After the phenomenal success of the 36th Chamber of Shaolin, San Te has decided to start 37th Chamber of Shaolin. The aim this time is to equip women with shaolin self-defence techniques.

The only condition for a woman to be eligible for the special training is that she must be between $10$ and $60$ years of age, inclusive of both $10$ and $60$.

Given the ages of $N$ women in his village, please help San Te find out how many of them are eligible for the special training.

### Input Format
- The first line of input contains a single integer $T$, denoting the number of test cases. The description of $T$ test cases follows.
- The first line of each test case contains a single integer $N$, the number of women.
- The second line of each test case contains $N$ space-separated integers $A_1, A_2,..., A_N$, the ages of the women.
### Output Format

For each test case, output in a single line the number of women eligible for self-defence training.

### Constraints
- $1 \leq T \leq 20$
- $1 \leq N \leq 100$
- $1 \leq A_i \leq 100$
### Sample 1:
Input
Output

```
3
3
15 23 65
3
15 62 16
2
35 9
```

```
2
2
1
```

### Explanation:

 **Test Case $1$** : Out of the women, only the $1^{st}$ and $2^{nd}$ women are eligible for the training because their ages lie in the interval $[10,60]$. Hence the answer is 2.

 **Test Case $2$** : Only the $1^{st}$ and $3^{rd}$ women are eligible for the training because their ages lie in the interval $[10,60]$. Hence the answer is again 2.

 **Test Case $3$** : Only the $1^{st}$ woman with age $35$ is eligible for the training. Hence the answer is $1$.

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-11-02T17:01:05.149Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
    // Fast I/O
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);

    int t;
    cin >> t;
    while(t--) {
        int n;
        cin >> n;
        int eligible_count = 0;

        for(int i = 0; i < n; i++) {
            int age;
            cin >> age;
            // Check if the age is between 10 and 60, inclusive
            if(age >= 10 && age <= 60) {
                eligible_count++;
            }
        }
        cout << eligible_count << "\n";
    }

    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/SELFDEF)