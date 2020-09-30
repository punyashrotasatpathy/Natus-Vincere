//Hello
#include <iostream>

using namespace std;

int main()
{
    int i, j, cur, l;
    long long fact, sum;
    cout<<"All Strong numbers between 1 to 1000 are"<<endl;
    for(i=1; i<=1000; i++)
    {
        cur = i;
        sum = 0;
        while(cur > 0)
        {
            fact = 1;
            l = cur % 10;
            for( j=1; j<=l; j++)
            {
                fact = fact * j;
            }
            sum += fact; 
            cur /= 10;
        }
        if(sum == i)
        {
            cout<<i<<endl;
        }
    }
