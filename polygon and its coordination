//
//  main.cpp
//  area test
//
//  Created by Haoyang Chen on 2020/11/2.
//

#include <iostream>
#include <cmath>
using namespace std;
int main(int argc, const char * argv[])
{
    int side;                                                                                                        //定义多边形的边数
    cout << "please enter the sides of your graph" <<endl;
    cin >> side ;
    char coor[side][2];                                                                                              //用数组记录多边形各个定点的坐标
    for (int i=0;i < side;i++)
    {
        cin >> coor[i][0] >> coor[i][1];
    }
    /*
     for (int i=0;i < side;i++)
    {
        int dist1=0;//点1到原点的距离
        int dist2=0;//点2到原点的距离
        dist1=sqrt(coor[i][0]*coor[i][0]+coor[i][1]*coor[i][1]);
        dist2=sqrt(coor[i+1][0]*coor[i+1][0]+coor[i+1][1]*coor[i+1][1]);
        
    }
     */
    for (int i=0;i <=side ;i++)
    {
    cout << coor[i][0] << "  " << coor[i][1] <<endl;
    }
    float area=0;                                                                                                               //定义面积
    float peri =0;                                                                                                              //定义周长
    for(int i=1;i<side-1;i++)
    {
        float a1=sqrt((coor[i][0]-coor[0][0])*(coor[i][0]-coor[0][0])+(coor[i][1]-coor[0][1])*(coor[i][1]-coor[0][1]));        //三角形的一条边长
        cout << "a1 = " << a1 << " ";
        float a2=sqrt((coor[i+1][0]-coor[0][0])*(coor[i+1][0]-coor[0][0])+(coor[i+1][1]-coor[0][1])*(coor[i+1][1]-coor[0][1]));//三角形的一条边长
        cout << "a2 = " << a2 << " ";
        float a3=sqrt((coor[i+1][0]-coor[i][0])*(coor[i+1][0]-coor[i][0])+(coor[i+1][1]-coor[i][1])*(coor[i+1][1]-coor[i][1]));//三角形的一条边长
        cout << "a3 = " << a3 <<endl;
        float p=(a1+a2+a3)/2;                                                                                                  //海伦公式的半周长
        float s=sqrt(p*(p-a1)*(p-a2)*(p-a3));                                                                                  //海伦公式
        cout << "triangle's size is " << s << endl;                                                                         //一次循环中的三角形面积
        area += s;
        peri+= a3;
    }
    peri+=sqrt((coor[1][0]-coor[0][0])*(coor[1][0]-coor[0][0])+(coor[1][1]-coor[0][1])*(coor[1][1]-coor[0][1]));
    peri+=sqrt((coor[side-1][0]-coor[0][0])*(coor[side-1][0]-coor[0][0])+(coor[side-1][1]-coor[0][1])*(coor[side-1][1]-coor[0][1]));
    cout << "the polygon's size is " << area << endl;
    cout << "the polygon's perimeter is " << peri <<endl;
    return 0;
}
