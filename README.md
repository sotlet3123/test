#include<bits/stdc++.h>
using namespace std;
int a[100],n;
int check()
{
	int r=n,l=1;
	while(r>=l)
	{
		if(a[r]!=a[l]) return 0;
		r--;
		l++;
	}
	return 1;
}
void in()
{
	if(check())
	{
		for(int i=1;i<=n;i++)
		{
			cout<<a[i]<<" ";
		}
		cout<<endl;
	}	
}
void solve(int i)
{
	for(int j=0;j<=1;j++)
	{
		a[i]=j;
		if(i==n ) in();
		else solve(i+1);
	}
}
int main()
{
	cin>>n;
	solve(1);
}
// SL3123