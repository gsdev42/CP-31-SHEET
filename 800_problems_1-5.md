## 1. Halloumi Boxes 
----

## 2. Line Trip
```cpp
#include<bits/stdc++.h>
using namespace std;
 
int maxdiff(int n, vector<long long>&a){
    //let first dist required be between point 0 and a1
    long long diff=a[0];
    for(int i=1;i<n;i++){
        diff= max(diff,abs(a[i]-a[i-1]));
    }
    return diff;
}
 
void f(int n, int x, vector<long long>&a){
    long long ans=0;
    int diff= maxdiff(n,a);
    int last_lap=2*abs(x-a[n-1]);
    ans=max(diff,last_lap);
    cout<<ans<<"\n";
 
}
 
int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    
    int t;
    if(!(cin>>t)) return 0;
 
    while(t--){
        int n,x;
        cin>>n>>x;
        vector<long long>a(n);
        for(int i=0; i<n;i++)cin>>a[i];
 
        f(n,x,a);
 
    }
    return 0;
    
}

```

----
## 3. Cover in Water

```cpp
#include<bits/stdc++.h>
using namespace std;
 
void f(int n, string s){
 bool continuos_3_empty_cells=false;
 int total_empty_cell=0;
 for(int i=0;i<n;i++){
    if(s[i]=='.' && i+1<n && s[i+1]=='.'&&i+2<n && s[i+2]=='.'){
        continuos_3_empty_cells=true;
        break;
    }
    if(s[i]=='.'){
        total_empty_cell++;
        }
    }
 
    if(continuos_3_empty_cells){
            cout<< 2 <<endl;
        }
    else{
        cout<< total_empty_cell<<endl;
    }
   
  }
 
int main(){
 
    int t;
    if(!(cin>>t)) return 0;
 
    while(t--){
        int n;
        cin>>n;
 
        string s;
        cin>>s;
        f(n,s);
    }
 
}
```
-----
## 4. Game With Integers
```cpp
#include <iostream>
#include<bits/stdc++.h> 
using namespace std;
 
bool firstWins(long long n){
    return (n %3!=0);
}
 
int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
 
    int t;
    cin>>t;
    while(t--){
        long long n;
        cin>> n;
 
        if(firstWins(n)){
            cout<<"First\n";
        }
        else{
            cout<<"Second\n";
        }
       
 
 
    }
     return 0;
}
```
-----
## 5. Jagged swaps
```cpp
#include<bits/stdc++.h>
using namespace std;
 
bool canSort(long long int arr[]){
    return((arr[0]==1));
}
 
int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
 
    int t;
    cin>>t;
 
    while(t--){
        long long n;
        cin>>n;
 
        long long arr[n];
        for(int i=0; i<n;i++){
            cin>>arr[i];
        }
        
        if(canSort(arr)){
            cout<<"YES\n";
        }
        else{
            cout<<"NO\n";
        }
 
    }
}
```
----

