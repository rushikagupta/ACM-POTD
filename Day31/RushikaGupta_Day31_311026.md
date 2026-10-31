# Description of Solution
We declare an array of size n and initialise it to 0. Then for each level X and Y can solve, we iterate through them and set them all to 1 (true) in the levels array. We then use another loop to check for a level which remains unmarked. If one such level is found, we output negative and exit. If no such level is found, we print the positive output. 

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin>>n;
    
    int x, y;
    int level[n] = {0};

    cin>>x;
    for (int i = 0; i<x; i++){
        int a;
        cin>>a;
        level[a-1] = 1;
    }

    cin>>y;
    for (int i = 0; i<y; i++){
        int a;
        cin>>a;
        level[a-1] = 1;
    }
    
    for (int i = 0; i<n; i++){
        if (!level[i]){
            cout<<"Oh, my keyboard!";
            return 0;
        }
    }
    
    cout<<"I become the guy.";
    
    return 0;
}
```