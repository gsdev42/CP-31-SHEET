## 6. Doremy's Paint 3
```cpp
#include<iostream>
#include <bits/stdc++.h>
using namespace std;

// frequency_map.rbegin()->second
// rbegin() → reverse iterator pointing to the largest key
// frequency_map.begin()->second
// begin() → iterator pointing to the smallest key
// ->second → value associated with that key (frequency)

bool isGood(long long arr[], int n){
    
    map<long long , long long> frequency_map;
    for(int i=0;i<n; i++){
        frequency_map[arr[i]]++;
    }
    if(frequency_map.size()>2){
        return false;
    }

    //get the freq of smallest and largest element
    long long freq1= frequency_map.begin()->second;
    long long freq2= frequency_map.rbegin()->second;

    //checking if arr is good or not
    if(freq1==freq2){
        return true;
    }
    if(n%2==1 && (abs(freq1-freq2))==1){
        return true;
    }
    else{
        return false;
    }

}

int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int t;
    cin>>t;

    while(t--){
        int n;
        cin>>n;
        long long arr[n];
        
        for(int i=0;i<n;i++){
            cin>>arr[i];
        }

        if(isGood(arr,n)){
            cout<<"Yes\n";
        }
        else{
            cout<<"No\n";
        }

    }
    return 0;
}
```
----
## 7. Don't Try to Count
```cpp
#include<bits/stdc++.h>
using namespace std;
//checking if s belong in x or not

bool checkSubstr(string x, string s){
    //if x (n)is smaller than s (m) then ofc its not substr
    if(x.size()<s.size()){
        return false;
    }

    // check thru x and s
    //n-m+1 is the length of the common component
    for(int i=0; i<(x.size()-s.size()+1);i++){  //n-m+1

        // Check if the substring of x starting at i with length of s (m) is equal to s
        if(x.substr(i,s.size())==s){
            return true;
        }
    }
    return false;

}

int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin>>t;
    while(t--){
        int n ,m;
        cin>>n;
        cin>>m;
        string x, s;
        cin>>x;
        cin>>s;

        //create strings representing x after 0 to 5 operations
        string x0=x;
        string x1= x0+x0;
        string x2= x1+x1;
        string x3= x2+x2;
        string x4= x3+x3;
        string x5 = x4+x4;

        long long ans= -1;

        if(checkSubstr (x0,s)){
            ans=0;
        }
        else if(checkSubstr (x1,s)){
            ans=1;
        }
        else if(checkSubstr (x2,s)){
            ans=2;
        }
        else if(checkSubstr (x3,s)){
            ans=3;
        }
        else if(checkSubstr (x4,s)){
            ans=4;
        }
        else if(checkSubstr (x5,s)){
            ans=5;
        }
        cout<<ans<<endl;

    }
    return 0;
}
```
----
## 8. How Much Does Daytona Cost?
```cpp
#include<bits/stdc++.h>
using namespace std;
bool isPopular(long long arr[],int n,int k){
    for(int i=0;i<n;i++){
        if(arr[i]==k){
            return true;
        }
    }
    return false;

}

int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin>>t;

    while(t--){
        long long n,k;
        cin>>n;
        cin>>k;
        long long arr[n];
        for(int i=0; i<n ;i++){
            cin>>arr[i];
        }
        if(isPopular(arr,n,k)){
            cout<<"YES\n";
        }
        else{
            cout<<"NO\n";
        }
       
    }
}
```
----
## 9. Goals of Victory
```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin>>t;


    while(t--){
        long long n;
        cin>>n;
        long long a[n];
        long long sum=0;

        for(int i=0;i<n-1;i++){
            cin>>a[i];
            sum+=a[i];
        }
        cout<<-1*sum<<endl;

    }
    return 0;
}
```
----
## 10. Target Practice
```cpp
```
----
