# Description of Solution
We traverse through the input string and find the number of lower case and upper case characters. We then find which type of characters are maximum and then iterate through the string to convert any character of the opposite kind to the required one. 

# Solution
```
#include <iostream>
using namespace std;

int main(){
    string s;
    cin>>s;

    int lower = 0, upper = 0;
    int n = s.length();

    for (int i = 0; i<n; i++){
        if (s[i]>=65 && s[i]<=90){
            upper+=1;
        }
        else{
            lower +=1;
        }
    }

    for (char &c : s) {
        if (upper > lower)
            c = toupper(c);
        else
            c = tolower(c);
    }

    cout << s;

    return 0;
}```
