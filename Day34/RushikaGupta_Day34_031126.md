# Description of Solution
The row() function calculates the number of cubes required for each level using the triangular number formula n*(n+1)/2. The program takes the total number of cubes as input, then uses a while loop to calculate the cubes required for successive levels while keeping track of the height. Finally, it prints the maximum number of levels that can be built.

# Solution
```#include <bits/stdc++.h>
using namespace std;

int row(int n){
    return n*(n+1)/2;
}

int main() {
    int n;
    cin>>n;

    int i = 0;
    int cubes = 0;
    while(cubes<n){
        cubes+=row(i+2);
        i++;
    }

    cout<<i;

    return 0;
}
```