# Description of Solution

This code finds the length of the longest strictly increasing contiguous subarray. First, it takes the size of the array and initializes length and maxLength to 1. It then reads the first element into prev and traverses the remaining elements using a for loop. If the current element (curr) is greater than the previous element (prev), it increments length; otherwise, it resets length to 1. The max() function updates maxLength whenever a longer increasing sequence is found. Finally, it updates prev with curr and prints maxLength as the answer.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int n;
    cin >> n;

    int length = 1;
    int maxLength = 1;
    int prev, curr;

    cin >> prev;

    for (int i = 1; i < n; i++) {
        cin >> curr;

        if (curr > prev) {
            length++;
        } else {
            length = 1;
        }

        maxLength = max(maxLength, length);
        prev = curr;
    }

    cout << maxLength;

    return 0;
}
```
