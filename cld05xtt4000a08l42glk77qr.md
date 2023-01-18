# Day 1 of 30 Days Of Code

Hi Everyone,

Here is the solution of [#Day1](https://www.linkedin.com/feed/hashtag/?keywords=day1&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7020840076897136640) of [#30daysOfCode](https://www.linkedin.com/feed/hashtag/?keywords=30daysofcode&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7020840076897136640) by [Newton School](https://www.linkedin.com/company/newtonschool/) & [Everyday Coders](https://30daysofcode.netlify.app)🚀

Problem name: Mall and Coupons  
Link: [https://lnkd.in/dpPk546m](https://lnkd.in/dpPk546m)

See my solution using a heap.  
✅Approach: Take the maximum price and apply a coupon on it if available.

```cpp
#include <bits/stdc++.h> // header file includes every Standard library
using namespace std;
#define ll long long 
int main() {
	ll n,k,x;
    cin >> n >> k >> x;
    priority_queue<ll>pq;
    for(ll i=0; i<n; i++){
        ll a;
        cin >> a;
        pq.push(a);
    }
    ll ans=0;
    while(1){
        ll cur=pq.top();
        if(k <=0)
        break;
        
        if(cur){
            pq.pop();
            int times = cur/x;
            if(times){
                if(times > k)
                    times=k;
                cur-= x*times;
                k-=times;
            }else{
                if(k >0){
                    cur=0;
                    --k;}
                else break;
            }
            pq.push(cur);
        }else
        break;

    }
    while(pq.size()){
        ans += pq.top();
        pq.pop();
    }
    cout << ans;
    return 0;
}
```

If you are a tech enthusiast and want to be part of this program👩🏻‍💻  
registrations are open✨

**Register Here:** [https://30daysofcode.netlify.app/](https://30daysofcode.netlify.app/)

**How to Submit Code:** [https://youtu.be/lhtgBI9wMCY](https://youtu.be/lhtgBI9wMCY)

Special Thanks to [Vaneela Khatri](https://www.linkedin.com/in/vaneela-khatri-838998220?miniProfileUrn=urn%3Ali%3Afs_miniProfile%3AACoAADesv6wB2LfjR7H5fiTxbvEiQiDtzuOpQHw&lipi=urn%3Ali%3Apage%3Ad_flagship3_detail_base%3Br52IBXoVQfK1mPwp0Rwdqw%3D%3D) for giving the solution.