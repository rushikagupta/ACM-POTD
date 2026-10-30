# Description of Solution
We use a loop to input pi and qi, and use a third array element ti, to calculate the difference between them. If that space is equal or greater than 2, then that space can be used, so we add one to the final count. 

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin>>n;
    
    int p[n], q[n], t[n];
    int count = 0;


    for (int i = 0; i<n; i++){  
        cin>>p[i]>>q[i];
        t[i] = q[i] - p[i];
        if (t[i]>=2){
            count++;
        }
    }

    cout<<count;
    
    return 0;
}
```