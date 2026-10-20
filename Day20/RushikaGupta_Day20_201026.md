# Description of Solution
After taking the string as input, we simply replace the first character of the string with its capitalised version. We then output the same string with the first character modified, if required.

# Solution
```
#include <iostream>
#include <cctype>
using namespace std;

int main(){

    string s;
    cin>>s;

    s[0] = toupper(s[0]);

    cout<<s;

    return 0;
}
```