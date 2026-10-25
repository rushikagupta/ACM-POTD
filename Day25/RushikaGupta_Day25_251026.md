# Descrription of Solution
We declare vectors with default value 0 for both arthur and alexander initially. Then after the input for their liked numbers is taken, each of those value is changed to 1 for both of them. After that we simply give the apple to arthur if it is a liked number for him, else it is given to alexander. 

# Solution
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, a, b;
    cin >> n >> a >> b;

    vector<int> arthur(n + 1, 0), alexander(n + 1, 0);

    for (int i = 0; i < a; i++) {
        int x;
        cin >> x;
        arthur[x] = 1;
    }

    for (int i = 0; i < b; i++) {
        int x;
        cin >> x;
        alexander[x] = 1;
    }

    for (int i = 1; i <= n; i++) {
        if (arthur[i])
            cout << 1 <<" ";
        else
            cout << 2<<" ";
    }

    cout << '\n';
    return 0;
}
```