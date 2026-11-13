# Description of Solution

Unless the piece is any of the corner squares, the moves the king has are 8. If the king is at one of the four corners of the chessboard then it can't move to 5 squares. But if it is at the rest of edges, then it will only have 3 restricted moves.

# Solution

```
#include <bits/stdc++.h>
using namespace std;

int main() {
    char c;
    int d;
    cin>>c>>d;

    int squares=8;

    if ((c=='a' || c=='h')&&(d==1||d==8)){
        squares-=5;
    } else if ((c=='a' || c=='h')||(d==1||d==8)){
        squares-=3;
    }

    cout<<squares;

    return 0;
}
```
