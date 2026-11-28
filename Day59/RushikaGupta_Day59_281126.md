# Description of Solution
In this code, we start by checking whether the output would lie in the first half or the second half of the sequence. If it lies in the first half, then we output the kth odd number. If it lies in the second half, then we subtract the number of numbers in first half and then output the new kth even number.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    long long n, k;
    cin >> n >> k;

    if (k <= (n + 1) / 2)
    {
        cout << 2 * k - 1;
    }
    else
    {
        k = k - ((n + 1) / 2);
        cout << 2 * k;
    }

    return 0;
}
```