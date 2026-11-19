# Description of Solution

We use an array to store all the data prices. We then sort this array in the ascending order. We start calculating the cost by adding the most negative numbers first and even if their is capacity we stop when we encounter positive costs.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n, m;
    cin >> n >> m;

    int cost = 0;
    int price[n];

    for (int i = 0; i < n; i++) {
        cin >> price[i];
    }

    sort(price, price + n);

    for (int i = 0; i < m; i++) {
        if (price[i] < 0) {
            cost += price[i];
        }
    }

    cout << -cost;

    return 0;
}
```
