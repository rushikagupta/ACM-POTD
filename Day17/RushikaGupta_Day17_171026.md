# Description of Solution:
First, read the four horseshoe colors. We need to find how many of them have the same color.
Since Valera needs four horseshoes of different colors, we count the number of distinct colors among the four horseshoes. A set can be used because it automatically stores only unique values.
Finally, subtract the number of distinct colors from 4. The result is the minimum number of horseshoes Valera needs to buy.

# Solution
```
#include <iostream>
#include <set>
using namespace std;

int main(){
    int s1, s2, s3, s4;
    cin>>s1>>s2>>s3>>s4;

    set<int> color = {s1, s2, s3, s4};

    cout<<4-color.size();

    return 0;
}
```
