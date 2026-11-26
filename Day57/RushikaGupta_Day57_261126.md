# Description of Solution
We use a 5x5 grid so that we can have treat all squares of the 3x3 grid actual and don't have to apply boundary checking conditions. Then for each square of the grid we count the number of toggles happening in all the surrounding squares which will affect it's position. Then based on whether it is even or odd we toggle the switch.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

void toggle(int &n)
{
    n = 1 - n;
}

int main()
{
    int grid[5][5] = {};

    for (int j = 1; j <= 3; j++)
    {
        for (int i = 1; i <= 3; i++)
        {
            grid[j][i] = 1;
        }
    }

    for (int j = 1; j <= 3; j++)
    {
        for (int i = 1; i <= 3; i++)
        {
            int a;
            cin >> a;

            if (a % 2 == 1)
            {
                toggle(grid[j][i]);
                toggle(grid[j - 1][i]);
                toggle(grid[j + 1][i]);
                toggle(grid[j][i - 1]);
                toggle(grid[j][i + 1]);
            }
        }
    }

    for (int j = 1; j <= 3; j++)
    {
        for (int i = 1; i <= 3; i++)
        {
            cout << grid[j][i];
        }
        cout << '\n';
    }

    return 0;
}
```