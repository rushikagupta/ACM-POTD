# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main(){
    int n;
    cin>>n;

    vector<int> a(n);
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    int minDiff = INT_MAX;
    int ans1 = 0, ans2 = 1;

    for (int i = 0; i < n; i++) {
        int j = (i + 1) % n;
        int diff = abs(a[i] - a[j]);

        if (diff < minDiff) {
            minDiff = diff;
            ans1 = i;
            ans2 = j;
        }
    }

    cout << ans1 + 1 << " " << ans2 + 1 << endl;

    return 0;
}
```
