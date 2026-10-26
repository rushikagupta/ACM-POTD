# Description of Solution
After taking the input, we multiply m and n to find the total size of the board. The maximum number of pieces that can fit on it is the integer quotient of the size of board divided by the size of one piece.

# Solution
```
#include <iostream>
using namespace std;
 
int main() {
    int m, n;
    cin>>m>>n;
    
    int size = m*n;
    cout<<size/2;
    return 0;
}

```
