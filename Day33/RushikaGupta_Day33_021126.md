# Description of Solution
By pattern observation, we find that the output of the function is n/2 when n is even and -(n+1)/2 when n is odd. We input n and then simply output the corresponding value after checking if n is even or odd.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long n;
    cin>>n;
    cout<<(n%2==0? n/2:-(n+1)/2);

    return 0;

}
```