# THREETOPICS - Rating 572

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-25T06:07:31.662Z  

```c_cpp
#include <bits/stdc++.h>
using namespace std;

int main() {
	// your code goes here
int t;
cin>>t;
while(t--){
  int a,b;
  cin>>a>>b;
  int c,d;
  cin>>c>>d;
  if (a<=c && b<=d){
      cout<<"possible"<<endl;
  } else 
      cout<<"impossible"<<endl;
}
}

```

---

[View on CodeChef](https://www.codechef.com/problems/THREETOPICS)