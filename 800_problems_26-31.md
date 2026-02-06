## 26. Serval and Mocha's Array
```cpp
```
----

## 27. One and Two
```cpp
#include <bits/stdc++.h>
using namespace std;

int f(int a[],int count_twos, int n){
    if(count_twos==0){
        return 1;
    }
    if(count_twos%2==1){
            return -1;
    }      
    int twos=0;
    int ans=0;
    for(int i=0;i<n;i++){
        if(a[i]==2){
            twos++;         
        }
        if(twos==count_twos/2){
            ans=i+1;
            break;
        }
    }
    return ans;
}

int main()
{     
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin >> t; 
    while (t--)
    {
        int n;
      
        cin >> n; 
        int a[n];

        int count_twos=0;
    
        for(int i=0;i<n;i++){
            cin>>a[i];
            if(a[i]==2){
                count_twos++;
            }
        }

        cout<<f(a,count_twos,n)<<endl;

    }
    
}

```
----

## 28. Make it Beautiful
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
        int n;
      
        cin >> n; 
        int a[n];
        for(int i=0;i<n;i++){
            cin>>a[i];
        }

        int max_el=a[n-1];
        int min_el=a[0];

        if(min_el==max_el){
            cout<<"NO"<<endl;
        }
        else{
            cout<<"YES"<<endl;
            cout<<a[n-1]<<" ";
            for(int i=0;i<n-1;i++){
                cout<<a[i]<<" ";
            }
            cout<<endl;
        }

    }
    
}

```
----

## 29. Everybody Likes Good Arrays!
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
        int n;
      
        cin >> n; 
        int a[n];
        for(int i=0;i<n;i++){
            cin>>a[i];
        }
        int count_ops=0;
        if(n==1){cout<<0<<endl;}
       else
       {for(int i=0; i<n-1;i++){
        if(a[i]%2==a[i+1]%2){
            count_ops++;
        }
        
       }
       cout<<count_ops<<endl;
       
    }

    }
    
}

```
----

## 30. Extremely Round
```cpp
#include <bits/stdc++.h>
using namespace std;

bool check(long long x){

    int count_digits=0;
    int count_zeroes=0;

    while(x!=0){
        if(x%10==0){
            count_zeroes++;
        }
        count_digits++;
        x/=10;
    }

    return(count_digits-count_zeroes==1);

}


int main()
{     
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    //precomputation logic 
    vector<long long>round_nums;
    for(long long i=1; i<=999999;i++){
        if(check(i)){
            round_nums.push_back(i);
        }
    }


    int t;
    cin >> t; 
    while (t--)
    {
        long long n;
        cin>>n;
        long long ans=0;
        for(int i=0;i<round_nums.size();i++){
            if(round_nums[i]<=n){
                ans++;
            }
            else{ break;}
        }
        cout<<ans<<endl;  
    }

}
    
```
----

## 31. Two Permutations
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
        long long n,a,b;
        cin >> n>>a>>b; 

        if(a+b+2<=n||(a==b && a==n&& b==n)){
            cout<<"Yes"<<endl;
        }
        else{cout<<"No"<<endl;}

    }
    
}

```
----
