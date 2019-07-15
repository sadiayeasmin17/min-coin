# min-coin
#include<iostream>
using namespace std;
int main()
{
    int n,d,swap,cl[50],i,owed,t[i];
    cin>>n;
    cout<<"enter denominations";
    for(i=0;i<n;i++)
    {
        cin>>cl[i];
    }
    for(i=0;i<n;i++)
    {
        for(d=0;d<n-i-1;d++)
        {
            if(cl[d]<cl[d+1])
            {
                swap=cl[d];
                cl[d]=cl[d+1];
                cl[d+1]=swap;
            }
        }
    }
    
    cout<<"enter the amount owed";
    cin>>owed;
    for(i=0;i<n;i++)
    {
        t[i]=owed/cl[i];
        owed%=cl[i];
    }
    for(i=0;i<n;i++)
    {
        cout<<cl[i]<<"*"<<t[i]<<"="<<cl[i]*t[i]<<endl;
    }
}
