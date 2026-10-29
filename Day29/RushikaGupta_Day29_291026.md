# Description of Solution
The program first takes an integer n as input and initializes row as n/2. It then uses a for loop to print the upper half of the pattern, where i increases by 2 in each iteration. For every row, the first inner loop prints stars on the left, the second inner loop prints D characters in the middle, and the third inner loop prints stars on the right. The number of stars decreases as the number of D characters increases. After printing the upper half, another loop prints n consecutive D characters to form the middle row. Finally, a reverse for loop prints the lower half by decreasing i by 2 in each iteration, using the same three inner loops to print stars on both sides and D characters in the middle. Each row ends with a newline, creating a symmetrical pattern.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin>>n;

    int row = n/2;

    for (int i = 1; i<=2*row; i+=2){
        for (int j = 0; j<((n-i)/2); j++){
            cout<<"*";
        }
        for (int j = 0; j<i; j++){
            cout<<"D";
        }
        for (int j = 0; j<(n-i)/2; j++){
            cout<<"*";
        }
        cout<<endl;
    }
    for (int i = 0; i<n; i++){
        cout<<"D";
    }
    cout<<endl;
    for (int i = 2*row-1; i>=1; i-=2){
        for (int j = 0; j<((n-i)/2); j++){
            cout<<"*";
        }
        for (int j = 0; j<i; j++){
            cout<<"D";
        }
        for (int j = 0; j<(n-i)/2; j++){
            cout<<"*";
        }
        cout<<endl;
    }
    return 0;
}
```