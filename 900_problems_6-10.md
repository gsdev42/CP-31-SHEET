## 6. Longest Divisors Interval
```cpp
```
----
## 7. Balanced Round
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
        long long  n,k;
        cin >> n>> k;
        vector<long long>a(n);
        for(int i=0; i<n;i++){
            cin>>a[i];
        }

        sort(a.begin(),a.end());
        
    
        long long cnt=1; // Initialize counter for the current sequence length
		long long largest_subarr=1; // Initialize the largest sequence length found
        for(int i=0; i<n-1;i++){
            if(a[i+1]-a[i]<=k){
                cnt++; //increment
            }
            else{
                cnt=1;
              
            } //reset

              largest_subarr= max(cnt,largest_subarr) ;
        }

        cout<<n-largest_subarr<<endl;


    }
    return 0;
    
}

```
----
## 8. Comparison String
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
        string s;
        cin>>s;

        int longest_substr_len=1;
        int curr_substr_len=1;
        for(int i=0;i<n-1;i++){
            if(s[i]==s[i+1]){
                curr_substr_len++;
            }
            else{
                longest_substr_len=max(curr_substr_len,longest_substr_len);
                curr_substr_len=1;
            }

            
        }
        //executing this part cuz towards the end we need to check the substr len again
        longest_substr_len=max(longest_substr_len,curr_substr_len);
        

        cout<<longest_substr_len+1<<endl;



    }
    return 0;
    
}

```
----
## 9. Permutation Swap
```cpp
#include <bits/stdc++.h>
#include <numeric>
using namespace std;

int main()
{     
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int t;
    cin >> t; 
    while (t--)
    {
        long long  n;
        cin >> n;
        vector<long long>a(n);
        for(int i=0; i<n;i++){
            cin>>a[i];
        }

        long long k= abs(a[0]-1);
    
        for(int i=1; i<n;i++){
           k = gcd(k, abs(a[i] - (i + 1)));
            
        }
        cout<< k<< endl;



    }
    return 0;
    
}

```
----
## 10. Odd Queries
```cpp
```
----
