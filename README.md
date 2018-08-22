 -Find-the-Number-which-contain-the-digit-d-
#include <bits/stdc++.h>
using namespace std;
void printNumbers(int n, int d);
int main()
 {
     int t;
 cin>>t;
 while(t--)
 {
	int n,d;
	cin>>n;
	cin>>d;
	if(n>=d)
	{
       printNumbers(n,d);
	}
	else
	{
	    cout<<"-1"<<"\n";
	}
	cout<<"\n";
 }
	return 0;
}
bool isDigitPresent(int x, int d)
{
    // Breal loop if d is present as digit
    while (x > 0)
    {
        if (x % 10 == d)
            break;
 
        x = x / 10;
    }
 
    // If loop broke
    return (x > 0);
}
 
// function to display the values
void printNumbers(int n, int d)
{
    // Check all numbers one by one
    for (int i = 0; i <= n; i++)
 
        // checking for digit
        if (i == d || isDigitPresent(i, d))
            cout << i << " ";
}
