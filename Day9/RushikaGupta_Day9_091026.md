# Solution
```
#include <iostream>
#include <cmath>
using namespace std;

bool tri(int n){
    if (n<0){
        return false;
    }

    int val = 8*n + 1;

    float root = sqrt(val);

    return (root*root == val);
}

int main(){
    int n;
    cin>>n;
    if (tri(n)){
        cout<<"YES";
    }
    else{
        cout<<"NO";
    }
}
```
