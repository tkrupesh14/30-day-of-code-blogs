# Day 3 of 30 Days Of Code

Hi everyone 👋🏻

Here is solution of #Day2 of #30daysofcode by @[Newton School](@newtonschool) & @[30 Days Of Code](@30daysofcode) 🚀

Problem name: **Edward and Maths Competition**

Link: [https://my.newtonschool.co/playground/code/0vb6uf9tra6m](https://my.newtonschool.co/playground/code/0vb6uf9tra6m)

✅Approach: Solved using simple maths concept. In series 1,2,...n, we've n/2 even numbers and (n/2)+1 odd numbers. So we'll multiply these to get the number of possible pairs.

If you are a tech enthusiast and want to be part of this program👩🏻‍💻  
registrations are open till 20th Jan✨

**Register Here:** [**30daysofcode.netlify.app**](http://30daysofcode.netlify.app)

**How to Submit Code:** [**youtu.be/lhtgBI9wMCY**](http://youtu.be/lhtgBI9wMCY)

```cpp
  #include <bits/stdc++.h>
  using namespace std;
  int main() {
      int n;
      cin >> n;
      int even = n/2;
      int odd = n-even;
      cout << even*odd;
      return 0;
  }
```