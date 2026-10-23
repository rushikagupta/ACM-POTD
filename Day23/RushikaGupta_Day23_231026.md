# Description of Solution
We declare integer variables to store the highest value, its index, and the second-highest value. After taking n as input, we iterate through the array, reading one element at a time. If the current element is greater than the highest value so far, we update the index, assign the previous highest value to the second-highest variable, and store the current element as the new highest. Otherwise, if it is greater than the second-highest value, we update the second-highest value. Finally, we output the index plus one to convert it to 1-based indexing, along with the second-highest value.

# Solution
```
#include <iostream>
using namespace std;

int main(){
    int n;
    int high = 0;
    int sec= 0;
    int index = 0;
    cin>>n;
    int arr[n];


    for (int i = 0; i<n; i++){
        cin>>arr[i];
        if (arr[i]>high){
            index = i;
            sec = high;
            high = arr[i];
        }
        else if (arr[i]>sec){
            sec = arr[i];
        }
    }

    cout<<index+1<<" "<<sec;

    return 0;
}
```