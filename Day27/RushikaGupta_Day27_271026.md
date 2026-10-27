# Description of Solution
We initialise an array of n characters to 0, and as we take inputs, we set each watched episode as 1 (in 0-indexed system). Then only one episode marked as zero remains, we loop through the array to find it and exit the code after it has been output.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin>>n;

    int ep[n] = {0};
    int num;

    for (int i = 0; i<n-1; i++){
        cin>>num;
        ep[num-1] = 1;
    }

    for (int i = 0; i<n; i++){
        if (ep[i] == 0){
            cout<<i+1;
            return 0;
        }
    }
}
```