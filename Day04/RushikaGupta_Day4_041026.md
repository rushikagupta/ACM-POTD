# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    long long d;
    cin >> n >> d;

    vector<long long> a(n);
    for (auto &x : a)
        cin >> x;

    long long ans = 0;

    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            if (abs(a[i] - a[j]) <= d) {
                ans += 2;
            }
        }
    }

    cout << ans << '\n';

    return 0;
}```
