# Description of Solution

We use a loop to output "I hate that" or "I love that" alternatingly for n-1 times. And then at the last we output "I hate it" or "I love it" based on whether n was even or odd.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin>>n;

    for (int i = 0;i<n-1; i++){
        cout<<(i%2==0?"I hate that ":"I love that ");
    }

    cout<<(n%2==0?"I love it":"I hate it");

    return 0;
}
```
