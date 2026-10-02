##Solution 
'''
#include <stdio.h>
 
int main() {
    int n, m;
    scanf("%d %d", &n, &m);
 
    char a[50][51];
 
    for (int i = 0; i < n; i++)
        scanf("%s", a[i]);
 
    int minRow = n, maxRow = -1;
    int minCol = m, maxCol = -1;
 
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            if (a[i][j] == '*') {
                if (i < minRow) minRow = i;
                if (i > maxRow) maxRow = i;
                if (j < minCol) minCol = j;
                if (j > maxCol) maxCol = j;
            }
        }
    }
 
    for (int i = minRow; i <= maxRow; i++) {
        for (int j = minCol; j <= maxCol; j++) {
            printf("%c", a[i][j]);
        }
        printf("\n");
    }
 
    return 0;
}
'''
