# Description of Solution

We simply use two integers to count the occurences of the two characters corresponding each of their names by incrementing them. We then compare the two numbers and output the corresponding value.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    string s;
    string out;

    int a = 0, d = 0;

    cin>>n>>s;
    for (int i = 0; i<n; i++){
        if (s[i]=='A'){
            a++;
        }else{
            d++;
        }
    }

    if (a>d){
        out="Anton";
    } else if (d>a){
        out ="Danik";
    } else{
        out="Friendship";
    }

    cout<<out;

    return 0;
}
```
