# Description of the Solution:
We iterate through all non-negative integer values of \(a\) such that \(a^2 \le n\). For each value, we calculate \(b = n - a^2\) and check whether \(a + b^2 = m\). If both equations are satisfied, we increment the counter. Finally, we print the total number of valid pairs \((a,b)\).

# Solution:
```
#include <iostream>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    int count = 0;

    for (int a = 0; a * a <= n; a++) {
        int b = n - a * a;

        if (a + b * b == m) {
            count++;
        }
    }

    cout << count;

    return 0;
}
```
