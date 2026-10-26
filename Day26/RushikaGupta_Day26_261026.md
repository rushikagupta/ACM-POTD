# Description of Solution
First, we take all the inputs, storing the volume of containers in an array. Now, using this array we find the sum of the array and the maximum value of the array. The game can be played without losing if the capacity of empty cup is equal to the sum of volumes of all containers, except one of the containers with maximum value. On checking this condition, we output the corresponding result.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, s;
    cin>>n>>s;

    int volumes[n];
    for (int i = 0; i<n; i++){
        cin>>volumes[i];
    }

    int max=volumes[0];
    for (int i = 1; i<n; i++){
        if (volumes[i]>max){
            max = volumes[i];
        }
    }

    int sum = 0;
    for (int i = 0; i<n; i++){
        sum+=volumes[i];
    }

    sum-=max;
    cout<<(sum<=s?"YES":"NO");

    return 0;
}
```