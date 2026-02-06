## 21. Blank Space

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{     
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin >> t; 
    while (t--)
    {
        long long n;
        cin >> n; 
        long long a[n];
        for (int i = 0; i < n; i++){ 
            cin >> a[i];
        }

    long long maxlen=0;
    long long count_zero=0;



        for(int i=0;i<n;i++){
          if(a[i]==0){
            count_zero++;
          }
          if(a[i]==1){
            count_zero=0;
          }
          
          maxlen=max(maxlen,count_zero);
          
            
        }
        cout<<maxlen<<endl;


    }
    
}

```
-----

## 22. Coins

```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{     
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin >> t; 
    while (t--)
    {
        long long n,k;
        cin >> n>>k; 

        if(n%2==0 || (n-k)%2==0){
            cout<<"YES\n";
        }

        else{cout<<"NO\n";}
    }
    
}

```
-----

## 23. Walking Master
```cpp
```
-----



## 24. We Need the Zero

```cpp
```
-----


## 25. Prepend and Append
```cpp
```
-----
