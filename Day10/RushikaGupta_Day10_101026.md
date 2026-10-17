# Description of Solution:
First, read the entire string using getline(). Traverse the string from the end and find the last alphabetic character. Convert it to lowercase and check whether it is a vowel (a, e, i, o, u) or y. If it is, print "YES"; otherwise, print "NO".

# Solution
```

#include <iostream>
#include <string>
#include <cctype>
using namespace std;

int main() {
    string question;
    getline(cin, question);

    for (int i = question.size() - 1; i >= 0; i--) {
        if (isalpha(static_cast<unsigned char>(question[i]))) {
            char ch = tolower(static_cast<unsigned char>(question[i]));

            if (ch == 'a' || ch == 'e' || ch == 'i' ||
                ch == 'o' || ch == 'u' || ch == 'y') {
                cout << "YES";
            } else {
                cout << "NO";
            }
            return 0;
        }
    }
}
```
