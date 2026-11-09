# Description of Solution

We input the variables, and then we find the whole number equal to or less than the division quotient of n/k. The next number greater than n, and divisible by k, is k multiplied by this quotient+1.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long n, k;
    cin>>n>>k;

    long long factor = n/k;
    cout<<k*(factor+1);

    return 0;
}
```
