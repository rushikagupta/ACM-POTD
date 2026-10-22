# Description of Solution
Brief description of the solution: The maximum number of cells that can contain a coder is \\(\lceil n^2/2 \rceil\\), calculated using `(n * n + 1) / 2`. We then fill the \\(n \times n\\) grid with an alternating pattern of `C` and `.`, placing `C` in cells where the sum of the row and column indices is even. This ensures that no two coders occupy adjacent cells horizontally or vertically.

# Solution
```

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    cout << (n * n + 1) / 2 << '\n';

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++)
            cout << ((i + j) % 2 == 0 ? 'C' : '.');

        cout << '\n';
    }

    return 0;
}
```