## Solution

```
#include <stdio.h>

int main() {
    int n, m;
    scanf("%d %d", &n, &m);

    char a[100][101];

    for (int i = 0; i < n; i++) {
        scanf("%s", a[i]);
    }

    for (int i = 0; i < n; i++) {

        // Check that the entire row has the same colour
        for (int j = 1; j < m; j++) {
            if (a[i][j] != a[i][0]) {
                printf("NO");
                return 0;
            }
        }

        // Check that this row differs from the next row
        if (i < n - 1 && a[i][0] == a[i + 1][0]) {
            printf("NO");
            return 0;
        }
    }

    printf("YES");
    return 0;
}
```