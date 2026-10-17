# Description of the Solution

First, read the string s. Iterate through it character by character. If the character is ., print 0. Otherwise, check the next character: if it is ., print 1; otherwise, print 2. After processing a pair, skip the next character.

# Solution
```
#include <iostream>
#include <string>
using namespace std;

int main()
{
    string s;
    cin >> s;

    for (int i = 0; i < s.length(); i++)
    {
        if (s[i] == '.')
        {
            cout << "0";
        }
        else
        {
            if (s[i + 1] == '.')
                cout << "1";
            else
                cout << "2";

            i++;
        }
    }

    cout << endl;

    return 0;
}
```
