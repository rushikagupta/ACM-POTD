# Description of Solution

We count the number of occurences of each digit in the sequence seperately. The minimum number of conversions required is the sum of all these counts and subtract the number with maximum occurences. We output this number.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n;
    cin >> n;

    int count1 = 0;
    int count2 = 0;
    int count3 = 0;

    for (int i = 0; i < n; i++) {
        int a;
        cin >> a;

        if (a == 1) {
            count1++;
        }
        else if (a == 2) {
            count2++;
        }
        else {
            count3++;
        }
    }

    int maxCount = count1;

    if (maxCount < count2) {
        maxCount = count2;
    }

    if (maxCount < count3) {
        maxCount = count3;
    }

    int sum = count1 + count2 + count3;

    cout << sum - maxCount;

    return 0;
}
```
