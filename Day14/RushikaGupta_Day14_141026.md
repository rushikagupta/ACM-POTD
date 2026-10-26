# Description of Solution
We read the scores of all participants and use the score of the \(k\)-th participant as the threshold. We then iterate through the scores and count participants whose scores are greater than or equal to this threshold and strictly positive. Finally, we output the total count.

# Solution
```
#include <iostream>
using namespace std;

int main() {
    int n, k;
    cin >> n >> k;

    int a[50];

    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    int count = 0;

    for (int i = 0; i < n; i++) {
        if (a[i] >= a[k - 1] && a[i] > 0) {
            count++;
        }
    }

    cout << count;

    return 0;
}
```
