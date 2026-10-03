## Solution 
```
#include <stdio.h>
#include <limits.h>

int main() {
    int n;
    scanf("%d", &n);

    int smallest = INT_MAX;
    int second = INT_MAX;

    for (int i = 0; i < n; i++) {
        int x;
        scanf("%d", &x);

        if (x < smallest) {
            second = smallest;
            smallest = x;
        } 
        else if (x > smallest && x < second) {
            second = x;
        }
    }

    if (second == INT_MAX)
        printf("NO");
    else
        printf("%d", second);

    return 0;
}
```
