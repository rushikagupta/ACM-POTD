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
