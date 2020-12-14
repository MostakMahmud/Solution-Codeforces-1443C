# Solution-Codeforces-1443C
Here our target is to get all the foods within minimum amount of time. As it is clear in case of getting delivary from the resturants it's all about the maximum time taken from the ones we want to get delivary from as they work in prallel. For an example let time taken by them is 4,9,6 so as described before within 9 min we will get all the food. So here our task is to minimize this time. First we have to sort these time. So initially the maximum possible result is the largest one. Now let's run a loop starting from the back and check upitl which point if petya goes to the resturant time is less than courier time. This way we can minimize the max value. And in the end we just have to find the maximum value betweem courier and petya's time.
#define encoding_898                 \
    ios_base::sync_with_stdio(false);\
    cin.tie(NULL);                   \
    cout.tie(NULL);                  \
    cerr.tie(NULL);
#include<bits/stdc++.h>
using namespace std;
#define ll long long
int main(void){
    encoding_898;
    int t;
    cin>>t;
    while(t--){
        int n,a;
        cin>>n;
        vector<pair<int,int>>vec;
        ll total_res=0,total_del=0;
        int x[n];
        for(int i=0;i<n;i++)
            cin>>x[i];
        for(int i=0;i<n;i++){
            cin>>a;
            vec.push_back({x[i],a});
        }
        sort(vec.begin(),vec.end());
        for(int i=n-1;i>=0;i--){
            if(total_res+vec[i].second>=vec[i].first){
                total_del=(ll)vec[i].first;
                 break;
            }
            else
                total_res+=vec[i].second;
        }
        ll ans=max(total_res,total_del);
        cout<<ans<<"\n";
    }
    return 0;
}
