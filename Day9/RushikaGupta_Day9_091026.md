# Solution

Beginner:
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

Intermediate:
```
#include <iostream>
#include <string>
using namespace std;

int main()
{
    long long n, m, a;
    cin>>n>>m>>a;

    long long length = (n+a-1)/a;
    long long width = (m+a-1)/a;

    cout<<length*width<<endl;

    return 0;
}
```

