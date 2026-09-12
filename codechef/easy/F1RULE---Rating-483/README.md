# F1RULE - Rating 483

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-12T07:51:55.145Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
	// your code goes here
int t;
cin>>t;
while(t--){
    int w,x,y,z;
    cin>>w>>x>>y>>z;
    if(w+y*z>x){
        cout<<"overFlow"<<endl;
    } else if (w+y*z<x) {
        cout<<"Unfilled"<<endl;
    } else
        cout<<"filled"<<endl;
}
}

```

---

[View on CodeChef](https://www.codechef.com/problems/F1RULE)