# Description of Solution

We use prime factorisation to count the number of distinct prime factors of each number from 2 to n. We repeatedly divides a number by each prime factor to avoid counting the same factor more than once. If a number has exactly two distinct prime factors, it is considered almost prime, and the final count is printed.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n;
    cin >> n;

    int ans = 0;

    for (int i = 2; i <= n; i++) {
        int x = i;
        int cnt = 0;

        for (int j = 2; j * j <= x; j++) {
            if (x % j == 0) {
                cnt++;

                while (x % j == 0) {
                    x /= j;
                }
            }
        }

        if (x > 1) cnt++;

        if (cnt == 2) ans++;
    }

    cout << ans;

    return 0;
}
```
