# Description of Solution
Firstly, we declare a user-defined function to check if the number is composite. In the main function, we use a loop to check all numbers from 1, and then calculate the other number by taking the difference. If both the numbers thus found are composite, then we print them and exit.

# Solution
```
#include <bits/stdc++.h>
using namespace std;

bool isComposite(int n);

int main() {
    int n;
    cin>>n;
    
    for (int i = 1; i<=n; i++){
        int j = n-i;
        if (isComposite(i)&&isComposite(j)){
            cout<<i<<" "<<j;
            return 0;
        }
    }
}

bool isComposite(int n) {
    if (n <= 3) return false;

    if (n % 2 == 0 || n % 3 == 0) return true;

    for (int i = 5; i * i <= n; i += 6) {
        if (n % i == 0 || n % (i + 2) == 0) {
            return true;
        }
    }

    return false;
}
```