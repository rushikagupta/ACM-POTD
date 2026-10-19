# Description of Solution
We increment the given year by 1 and check whether all its digits are distinct. We convert the year into a string and use a set to store its digits. If the set size equals the string length, all digits are unique, so we print the year and stop. Otherwise, we continue checking the next year until we find the smallest valid year.

# Solution:
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int y;
    cin >> y;

    while (true) {
        y++;

        string s = to_string(y);
        set<char> digits(s.begin(), s.end());

        if (digits.size() == 4) {
            cout << y << '\n';
            break;
        }
    }

    return 0;
}

```
