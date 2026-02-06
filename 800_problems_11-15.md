## 11. Ambitious Kid
```cpp
#include<bits/stdc++.h>
using namespace std;
 
int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
 
    
        long long n;
        cin>>n;
        vector<long long> a(n);
        for (int i = 0; i < n; i++) {
            cin >> a[i];
        }
        long long min_ops=INT_MAX;
        
        for(int i=0;i<n;i++){
            min_ops=min(min_ops,abs(a[i]));
            
        }
        cout<<min_ops<<endl;
  
    return 0;
}
```
----
## 12. Sequence Game
```cpp
```
----
## 13. United We Stand
```cpp
```
----
## 14. Buttons
```cpp
```
----
## 15. Array Coloring
```cpp
```
----
