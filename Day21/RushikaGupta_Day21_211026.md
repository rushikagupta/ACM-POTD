# Description of Solution
We count the occurrences of 1, 2, and 3 in the input string, ignoring the + signs. Then, we print all the 1s first, followed by the 2s and 3s, adding + signs between the numbers. This produces the sum in sorted order as required.

# Solution
```
#include <iostream>
#include <string>
using namespace std;

int main() {
    string s;
    cin >> s;

    int a = 0, b = 0, c = 0;

    // Count the numbers, ignoring '+'
    for (char ch : s) {
        if (ch == '1')
            a++;
        else if (ch == '2')
            b++;
        else if (ch == '3')
            c++;
    }

    // Print the numbers in sorted order
    bool first = true;

    for (int i = 0; i < a; i++) {
        if (!first) cout << '+';
        cout << '1';
        first = false;
    }

    for (int i = 0; i < b; i++) {
        if (!first) cout << '+';
        cout << '2';
        first = false;
    }

    for (int i = 0; i < c; i++) {
        if (!first) cout << '+';
        cout << '3';
        first = false;
    }

    cout << '\n';
    return 0;
}
```
