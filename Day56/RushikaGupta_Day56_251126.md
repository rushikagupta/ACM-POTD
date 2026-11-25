# Description of Solution
We run the same process for all the n pair values entered. We run each iteration till at least one of the numbers become zero. And in each iteration for the process, we add to count the number of times the smaller number can be subtracted from the larger one. We then change the larger number to the remainder.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n;
    cin >> n;

    for (int i = 0; i < n; i++)
    {
        long long a, b;
        long long count = 0;
        cin >> a >> b;
        while (!(a == 0 || b == 0))
        {
            if (a > b)
            {
                count += a / b;
                a = a % b;
            }
            else
            {
                count += b / a;
                b = b % a;
            }
        }
        cout << count << endl;
    }

    return 0;
}
```