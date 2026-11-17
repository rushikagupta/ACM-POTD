# Description of Solution

In this solution, we store all the (a, b) pairs and then sort the containers in decreasing order of their b values. After that we start taking the containers with the maximum possible number of matches in them. We output the summation of that number multiplied by the matches in the corresponding box.

# Solution

```

#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    vector<pair<int, int>> v(m);

    for (int i = 0; i < m; i++) {
        int a, b;
        cin >> a >> b;
        v[i] = {b, a};
    }

    sort(v.rbegin(), v.rend());

    long long ans = 0;

    for (int i = 0; i < m && n > 0; i++) {
        int take = min(n, v[i].second);

        ans += 1LL * take * v[i].first;
        n -= take;
    }

    cout << ans << '\n';

    return 0;
}
```
