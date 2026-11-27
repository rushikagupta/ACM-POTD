# Description of Solution
The code checks whether Ksusha can reach the last sector by finding the maximum number of consecutive rocks in the road. It initializes a counter l to 1 and increments it whenever a rock is encountered, updating maxL to store the longest consecutive sequence. Whenever an empty sector is found, the counter resets to 1. Finally, it compares maxL with the maximum jumping distance k.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n, k;
    cin >> n >> k;

    string s;
    int l = 1;
    int maxL = 0;

    cin >> s;
    int p = s.size();

    for (int i = 0; i < p; i++)
    {
        if (s[i] == '#')
        {
            l++;
            if (maxL < l)
            {
                maxL = l;
            }
        }
        else
        {
            l = 1;
        }
    }

    cout << (maxL <= k ? "YES" : "NO");

    return 0;
}
```