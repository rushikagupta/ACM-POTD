# Description of Solution:
First, we input the number of elements \(n\) and store the colors in an array. Then, we iterate through the array and compare each element with the next element. If two consecutive elements have the same color, we increase the counter by one. After checking all adjacent pairs, we output the final value of the counter, which represents the number of consecutive equal-color pairs in the array.

# Solution:
```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<char> color(n);

    for (int i = 0; i < n; i++) {
        cin >> color[i];
    }

    int count = 0;

    for (int i = 0; i < n - 1; i++) {
        if (color[i] == color[i + 1]) {
            count++;
        }
    }

    cout << count << '\n';

    return 0;
}
```
