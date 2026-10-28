# Description of Solution
We use getline to take the input as a string due to whitespaces and find it's length. We then iterate through it's length and add to set all the lowercase alphabets. Then we return the set length because a set only stores unique values.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    string s;
    getline(cin, s);
    int n = s.length();
    set<char> unique;

    for (int i = 0; i<n; i++){
        if (s[i]>=97 && s[i]<=122){
            unique.insert(s[i]);
        }
    }

    cout<<unique.size();
    return 0;
}
```