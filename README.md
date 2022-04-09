#include<iostream>
using namespace std;
// Function to print given string in cross pattern
// Length of string must be odd
void printPattern(string str)
{
    int len = str.length();
    int i,j,k;
    k=(len + 1)/2;
    for (int i=1; i<=k; i++)
    {
        for(int j=k;j>=(i-1)*2-1;j--)
        cout<<" ";
        cout<<str[i];
        for(j=2;j<=(i-1)*4;j++)
        cout<<" ";
        if(i>1)
        cout<<str[i];
        cout<<"\n";
    }
    for(i=k-1;i>=1;i--)
    {
        for(j=k;j>=(i-1)*2-1;j--)
        cout<<" ";
        cout<<str[i];
        for(j=2;j<=(i-1)*4;j++)
        cout<<" ";
        if(i>1)
        cout<<str[i];
        cout<<"\n";
    }
}
int main()
{
    printPattern("racecar");
    return 0;
}
