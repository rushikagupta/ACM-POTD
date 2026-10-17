# Description of Solution
First, read n and the distances between consecutive cities. Then, read the starting city a and destination city b. Use a loop to add the distances from city a to city b-1. Finally, print the total distance in years.

# Solution
```
#include <iostream>
using namespace std;

int main(){
    int n;
    cin>>n;

    int d[n-1];
    for (int i = 0; i<n-1;i++){
        cin>>d[i];
    }

    int a, b;
    cin>>a>>b;

    int years=0;

    for (int i = a-1; i<b-1; i++){
        years+=d[i];
    }

    cout<<years;

    return 0;
}
```
