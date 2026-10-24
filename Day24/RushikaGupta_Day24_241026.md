# Description of Solution
After taking input of the string, we declare boolean variables for three conditions and set them to false. After checking the length conidition, we itireate through the string and set the conditions to true if they are met. Finally print the output if all the conditions are met.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    cin >> s;

    bool upper = false;
    bool lower = false;
    bool digit = false;

    int slength = s.length();

    if (slength < 5) {
        cout << "Too weak";
        return 0;
    }

    for (int i = 0; i < slength; i++) {
        if (s[i] >= '0' && s[i] <= '9') {
            digit = true;
        }
        else if (s[i] >= 'A' && s[i] <= 'Z') {
            upper = true;
        }
        else if (s[i] >= 'a' && s[i] <= 'z') {
            lower = true;
        }
    }

    bool strength = digit && upper && lower;

    cout << (strength ? "Correct" : "Too weak");

    return 0;
}
```