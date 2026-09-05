# ASSIGNMNT - Rating 467

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

_Description not available._

## Solution

**Language:** c_cpp  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-09-05T18:22:05.781Z  

```c_cpp
#include <iostream>
using namespace std;

int main() {
	// your code goes here
	int i ;
	int a[4];
	int c=0;
	for(i=0;i<4;i++)
	{
	    cin>>a[i];
	}
	for(i=0;i<4;i++)
	{
	    if(a[i]>=10)
	        c++;
	        
	}
	cout<<c<<endl;
	return 0;
}
```

---

[View on CodeChef](https://www.codechef.com/problems/ASSIGNMNT)