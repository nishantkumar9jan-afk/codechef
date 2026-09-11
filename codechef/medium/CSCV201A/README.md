# CSCV201A

![Difficulty](https://img.shields.io/badge/Difficulty-Medium-yellow)

## Problem

### Module on basic conditional statements

We have reviewed programming problems on basic math in the previous module.
We now incorporate conditional statements in our problem solving capabilities along with basic math.

Just a recap on what we covered in Learn C++ learning path regarding conditional statements.

- "if" and "else" can be used together to create conditions.
- The "else if" keyword means "if the previous conditions were not true, then try this condition"
- The "else" keyword includes all cases which aren't included in the previous conditions.
- Usual conditions used within if / else / else if statements Equals: a == b Not Equals: a != b Less than: a < b Less than or equal to: a <= b Greater than: a > b Greater than or equal to: a >= b
- "and" and "or" statements help check multiple conditions. "&&" can also be used to mean "and". "||" can also be used to mean "or".

Revise some of this syntax in the IDE.

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-11T08:10:51.723Z  

```c_cpp
// Click on 'Submit' to first see the results
// Click on 'Next to continue'
// if-else statements 
#include <bits/stdc++.h>

using namespace std;
int main()
{
    int a = 13;
    int b = 15;
    if (a >= b)
    {
        cout << a << " is greater than or equal to " << b << endl;
    }
    else
    {
        cout << a << " is lesser than " << b << endl;
    }

    // lets add the else if statement
    a = 14;
    b = 14;
    if (a > b)
    {
        cout << a << " is greater than " << b << endl;
    }
    else if (a == b)
    {
        cout << a << " is equal to " << b << endl;
    }
    else
    {
        cout << a << " is lesser than " << b << endl;
    }
    return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/CSCV201A)