
/*-----------------With the name of ALLAH--------------*/

#include<bits/stdc++.h>
using namespace std;

#define ll long long
#define dl double
#define sf scanf
#define pf printf

#define MS0(x) memset(x,0,sizeof(x))
#define MS1(x) memset(x,1,sizeof(x))
#define SORT(a,n) sort(begin(a),begin(a)+n)
#define REV(a,n) reverse(begin(a),begin(a)+n)

#define loop(i,ini,n) for(ll i=ini;i<=n;i++)
#define rloop(i,ini,n) for(ll i=ini;i>=n;i--)
#define rev_vector(a,n) reverse(begin(a),begin(a)+n)

vector<ll> graph[10002];

//-----dfs function-------------------

ll dfs(ll src)
{
	bool visited[10001]={0};
	stack<ll> s;

	s.push(src);
	visited[src]=true;

	ll c=1;
	while(!s.empty())
	{
		ll u=s.top();
		s.pop();
		loop(j,0,graph[u].size()-1)
		{
			ll v=graph[u][j];
			if(!visited[v])
			{
				s.push(v);
				visited[v]=true;
				c++;
			}
		}
	}
	return c;
}


int main()
{
    //freopen("inp.txt","r",stdin);
    ll N,E,x,y;
    while(sf("%lld %lld",&N,&E)==2)
    {	
    	MS0(graph);
		loop(i,1,E)
		{
			sf("%lld %lld",&x,&y);

			graph[x].push_back(y);
			graph[y].push_back(x);
		}

		ll nodes=dfs(x);
		if(nodes==N && E==N-1)	// "nodes==N" portion confirms no node is missing and grpah is not disconnected
			pf("YES\n");
		else
			pf("NO\n");
    }
    return 0;
}
