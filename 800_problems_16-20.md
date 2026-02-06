## 16. Desorting
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
 
        long long min_ops=INT_MAX;
 
        for(int i=0;i<n-1;i++){
            if(a[i]<=a[i+1]){
                //checking if the current pair is sorted or not
                long long diff=abs(a[i]-a[i+1]);
                long long ops=(diff/2)+1;
                min_ops= min(min_ops,ops);
            }
            else{min_ops=0;}
        }
        cout<<min_ops<<endl;
 
 
    }
    
}
```
----
## 17. Forbidden Integer
```cpp
```

----
## 18. Grasshopper on a Line
```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int t;
    cin>>t;
    while(t--){
        long long x;
        cin>>x;
        long long k;
        cin>>k;

        if(x%k==0){
            cout<<2<<endl;
            cout<<1<<" "<<x-1<<endl;
        }
        else{
            cout<<1<<endl;
            cout<<x<<endl;
        }
    }
    return 0;
}
```

----
## 19. Unit Array
```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int t;
    cin>>t;
    while(t--){
        int n;
        cin>>n;
       int a[n];

       int count_neg=0;
       int count_pos=0;

        for(int i=0; i<n;i++){
            cin>>a[i];
            if(a[i]==-1){
                count_neg++;
            }
            if(a[i]==1){
                count_pos++;
            }
        }
        
        long long ops=0;
        while(count_pos<count_neg || count_neg%2==1){
            ops++;
            count_neg--;
            count_pos++;
        }
        cout<<ops<<endl;

    }
    return 0;

}

```

----
## 20. Twin Permutations
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
        long long b[n];
        for (int i = 0; i < n; i++){ 
            cin >> a[i];
        }

    //let c=n+1 , we will use it to make ai+bi constant
    //bi=c-ai;
     
    long long c=n+1;


        for(int i=0;i<n;i++){
            b[i]=c- a[i];
            cout<<b[i]<<" ";
            
        }
        cout<<endl;


    }
    
}

```
----
