# Description of Solution
We return false if the length of the string is less than 7. If it is greater, we further check the conditions. For each character same as the next one we add one to the length and if it exceeds 7 we declare it dangerous. 

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main()
{
    string s;
    cin >> s;

    int n = s.size();

    bool isDang = false;

    if (n < 7)
    {
        cout << "NO";
    }
    else
    {
        int length = 1;
        for (int i = 0; i < n - 1; i++)
        {
            if (s[i] == s[i + 1])
            {
                length++;
                if (length >= 7)
                {
                    isDang = true;
                    break;
                }
            }
            else
            {
                length = 1;
            }
        }
        cout << (isDang ? "YES" : "NO");
    }

    return 0;
}
```