# Description of Solution

We sort all the nubers written on cards as they are input, and then the sum of numbers will be equal if we keep taking the same forward and backward.

# Solution

```
    #include <bits/stdc++.h>
    using namespace std;

    int main() {
        int n;
        cin >> n;

        vector<pair<int, int>> cards;

        for (int i = 0; i < n; i++) {
            int x;
            cin >> x;
            cards.push_back({x, i + 1});
        }

        sort(cards.begin(), cards.end());

        for (int i = 0; i < n / 2; i++) {
            cout << cards[i].second << " "
                << cards[n - 1 - i].second << endl;
        }

        return 0;
    }
```
