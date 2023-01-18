# Day 2 of 30 Days Of Code

Hi everyone 👋🏻

Here is solution of #Day2 of #30daysofcode by @[Newton School](@newtonschool) & @[30 Days Of Code](@30daysofcode) 🚀

Problem name: Friends Or Not? !

Link: [https://my.newtonschool.co/playground/code/nru0grk3qnkr](https://my.newtonschool.co/playground/code/nru0grk3qnkr)

✅Approach: Used an Undirected graph. If any node has (n-1) neighbors then the output will be YES else NO.

If you are a tech enthusiast and want to be part of this program👩🏻‍💻  
registrations are open till 20th Jan✨

**Register Here:** [**https://30daysofcode.netlify.app/**](https://30daysofcode.netlify.app/)

**How to Submit Code:** [**https://youtu.be/lhtgBI9wMCY**](https://youtu.be/lhtgBI9wMCY)

```cpp
#include <bits/stdc++.h> // header file includes every Standard library
using namespace std;

bool solve(vector<vector<int>> &adj, int n){
    for(auto ele : adj){
        if(ele.size() == n-1)
            return true;
    }
    return false;
}
int main() {
    int n;
    cin >> n;
    vector<vector<int>> adj(n+1);
    int u,v;
    for(int i=1; i<n; i++){
        cin >> u >> v;
        adj[u].push_back(v);
        adj[v].push_back(u);
    }
    bool ans = solve(adj,n);
    if(ans)
        cout << "Yes";
    else 
        cout << "No";
    return 0;
}
```