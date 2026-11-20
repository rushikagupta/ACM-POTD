# Description of Solution

We use getline() to get both the values as one and then use a set to store them all. This automatically filters out the repeated entries. We output the size of this set.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n;

    cin>>n;

    set<string> names;

    for (int i = 0; i<n; i++){
        string a;
        getline(cin>>ws, a);
        names.insert(a);
    }

    cout<<names.size();

    return 0;
}
```
