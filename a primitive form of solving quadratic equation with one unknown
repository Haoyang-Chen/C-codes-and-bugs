//
//  main.cpp
//  task 1
//
//  Created by Haoyang Chen on 2020/10/22.
//

#include <iostream>
#include <cmath>
using namespace std;
int main(int argc, const char * argv[])
{
    float a,b,c;
    float delta,x1,x2;
    cout << "输入3个系数a（a！=0），b，c：" << endl;
    cin >> a >> b >> c;
    cout << "a = " << a << '\t' << "b = " << b << '\t' << "c = " << c << endl;
    delta =b*b-4*a*c;
    if (delta == 0)
        {
            cout << "方程有两个相同实根：" ;
        }
    else if (delta > 0)
        {
            delta = sqrt(delta);
            x1 = (-b+delta)/(2*a);
            x2 = (-b-delta)/(2*a);
            cout << "方程有两个不同实根：" ;
            cout << "x1 = " << x1 << '\t' <<"x2 = " << endl;
        }
        else cout << "方程无实根！" << endl;   //delta < 0
    return 0;
}
