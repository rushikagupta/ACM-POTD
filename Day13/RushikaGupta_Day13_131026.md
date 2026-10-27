# Description of Solution
We convert both strings to uppercase to make the comparison case-insensitive. Then, we compare the characters at each position in order. If a character in the first string is greater than the corresponding character in the second, we print 1; if it is smaller, we print -1. If all corresponding characters are equal, we print 0.

# Solution
```
#include <iostream>
#include <string>
#include <cctype>
using namespace std;

int main() {
    string s1, s2;
    cin>>s1>>s2;
    for (char &c : s1) {
        c = toupper(c);
    }

    for (char &c : s2) {
        c = toupper(c);
    }

    int n = s1.length();
    for (int i = 0; i<n; i++){
        if ((int)s1[i] > (int)s2[i]){
            cout<<1;
            return 0;
        }
        if ((int)s1[i] < (int)s2[i]){
            cout<<-1;
            return 0;
        } 
    }
    cout<<0;
    return 0;
}
```
