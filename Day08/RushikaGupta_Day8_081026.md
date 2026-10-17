# Description of Solution
First, read the two strings s and t. If their lengths are different, print "NO". Otherwise, compare each character of s with the corresponding character of t in reverse order. If any characters differ, print "NO"; if all match, print "YES".

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main(){
    string s, t;
    cin>>s>>t;

    int n = s.length();

    if (t.length() != n) {
        cout << "NO";
        return 0;
    }

    for (int i = 0; i<n; i++)
    {
        if (s[i] != t[n-i-1])
        {
            cout<<"NO";
            return 0;
        }
    }

    cout<<"YES";
    
    return 0;
}
```
