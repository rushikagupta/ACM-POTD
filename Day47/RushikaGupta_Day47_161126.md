# Description of Solution

We use two prev and curr to compare the adjacent numbers for the entire array. We then use a while loop to add to the curr number to make it greater than prev. We append to count everytime we add d and finally assign curr to prev and input the next number.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    long long n, d;
    cin >> n >> d;

    long long count = 0;
    long long prev, curr;

    cin >> prev;

    for (int i = 1; i < n; i++)
    {
        cin >> curr;

        if (curr <= prev)
        {
            long long x = (prev - curr) / d + 1;
            curr += x * d;
            count += x;
        }

        prev = curr;
    }

    cout << count;

    return 0;
}
```
