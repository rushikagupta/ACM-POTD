## Description of the Solution
First, read n and initialize smallest and second to INT_MAX. Then, loop through the elements and update smallest and second to find the two smallest distinct values. If no second smallest value exists, print "NO"; otherwise, print second.

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
