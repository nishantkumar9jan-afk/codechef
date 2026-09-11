# CSCV201A

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

### Review syntax usage

Let us cover the 'conditional statements' syntax required for solving beginner's programming problems.

### Task

Write a program which does the following

- Accepts the count of test cases - $t$ Each test case has one integer $N$
- Output the following for each test case If input is less than or equal to $100$, output 'Good' If input is greater than 100 but less than or equal to $200$, output 'Better' If the input is greater than 200, output 'Best'
### Sample 1:
Input
Output

```
3
100
200
201
```

```
Good
Better
Best
```

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-11T08:11:46.868Z  

```c_cpp
// Solution as follows
#include <bits/stdc++.h>

using namespace std;
int main()
{
    int t;
    cin >> t;
    while (t--)
    {
        int N;
        // Accept 1 integer as input.
        cin >> N;
        //Check if N is less than or equal to 100
        if (N <= 100)
        {
            cout << "Good" << endl;
        }
        //2nd condition in the problem
        else if (N > 100 && N <= 200)
        {
            cout << "Better" << endl;
        }
        //3rd condition in the problem
        else
        {
            cout << "Best" << endl;
        }
    }
    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/CSCV201A)