# Description of Solution
The variables are declared using long long due to the given constraints of the variables. We input them and then calculate the total cost of the bananas. We then calculate the difference, or put it as 0 if he already has enough balance. Output the result.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    long long k, n, w;
    cin >> k >> n >> w;

    long long cost = k * w * (w + 1) / 2;
    long long difference = max(0, cost - n);

    cout << difference;

    return 0;
}
```