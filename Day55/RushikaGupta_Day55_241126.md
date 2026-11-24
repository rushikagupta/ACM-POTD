# Description of Solution
In this solutin we start by comparing n and k, if k is greater than n, then no solution can exist so we return -1. In other cases we start by making a vector of all n elements and then sorting them, in this way the area with k dates will be the one which lies between the (k-n)th sqaure and (k-n-1)th sqaure.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n, k;
    cin >> n >> k;

    if (k > n)
    {
        cout << -1;
    }
    else
    {
        vector<int> coord;
        for (int i = 0; i < n; i++)
        {
            int a;
            cin >> a;
            coord.push_back(a);
        }

        sort(coord.begin(), coord.end());

        cout << coord[n - k] << " " << coord[n - k];
    }
    return 0;
}
```