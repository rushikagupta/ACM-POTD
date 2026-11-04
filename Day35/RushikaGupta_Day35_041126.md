# Description of Solution
In this problem we use a set to store the lower case version of all letters being input as a part of the string. Since set only stores unique values, we find the size of the set and if it is not 26, it means some letter is missing.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main(){
    int n;
    cin>>n;

    string s;
    cin>>s;

    set<char> unique;

    for (int i = 0; i<n; i++){
        unique.insert(tolower(s[i]));
    }

    cout<<(unique.size()<26?"NO":"YES");

    return 0;
}
```