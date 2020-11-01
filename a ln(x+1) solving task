//
//  main.cpp
//  cos的计算
//
//  Created by Haoyang Chen on 2020/10/30.
//

#include <iostream>
#include<cmath>
using namespace std;
int main(int argc, const char * argv[])
{
    float x;
    float y=1;
    float sum=0;
    cout << "please enter x" << endl;
    cin >> x ;
    int l = -1;
    float k=1;
    int a=1;
    /*do
    {
        l=(-1)*l;
        k=k*x;
        y=k/(a*l);
        sum+=y;
        a++;
    }while(fabs(y)>1e-5);*/
    for(int a=1;;a++)
    {
        l=-1*l;
        k=k*x;
        y=k/(a*l);
        sum+=y;
     if(fabs(y)<1e-5)
       {
           break;
       }
    }
    cout << "ln(1+x)=" << sum << endl;
    return 0;
}
