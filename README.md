#include <iostream>
#include <math.h>
#include <stdlib.h>

using namespace std;
int main()
{
	int n;
	cin>>n;
	bool is_prime=true;
	//2是唯一一个为质数的偶数，所以后面去考察质数时略过偶数 
	cout<<2<<endl;
	for(int i=3;i<=n;i+=2)
	{
		is_prime=true;
		//考察每一个数是否是质数 
		for(int j=3;j<=sqrt(i);j++)
		{
			if(i%j==0)
			{
				is_prime=false;
				break;
			}
		}
		if(is_prime)
		{
			cout<<i<<endl;
		}
	}
	return 0;
} 
