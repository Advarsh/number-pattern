/*# number-pattern
code for number pattern
4 4 4 4 4 4 4
4 3 3 3 3 3 4
4 3 2 2 2 3 4
4 3 2 1 2 3 4
4 3 2 2 2 3 4
4 3 3 3 3 3 4
4 4 4 4 4 4 4
*/

#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n=4, t=n*2, r1, r2, n1, n2=2, temp=2;
    n1=n;
    
    for(int i=1; i<t; i++)
    {
        if(i<=n)
        {
            r1=i; r2=t-i;//1, 7. 2,6.
            for(int j=1; j<t; j++)
            {
                if(j>=r1 && j<=r2){
                    cout<<n1<<" ";
                }
                else{
                    cout<<abs((n-j))+1<<" ";//
                }
            }
            n1--;
            cout<<endl;
        }  
        else
        {
            r1=i-n2; r2=i;
            for(int j=1; j<t; j++)
            {
                if(j>=r1 && j<=r2){
                    cout<<temp<<" ";
                }
                else{
                    cout<<abs((n-j))+1<<" ";//
                }
            }
            temp++;
            n2=n2+2;
            cout<<endl;
        }
    }
    return 0;
}
