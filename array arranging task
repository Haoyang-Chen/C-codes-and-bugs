//
//  main.cpp
//  array arranging task
//
//  Created by Haoyang Chen on 2020/10/28.
//

#include <iostream>
using namespace std;
int main(int argc, const char * argv[])
{
    int arr[10];
    cout << "please enter an array of 10 numbers" << endl;
    for(int o = 0;o <10;o++)
    {
        cin >> arr[o];
    }
    cout << "the former array is as follows" << endl;
    for(int b = 0;b<sizeof(arr)/sizeof(arr[0]);b++)
    {
        cout << arr[b];
    }
    cout << endl;
    int i = sizeof(arr)/sizeof(arr[0]-1);
    for(int a=0;a<i;a++)
    {
        for(int j=0; j < sizeof(arr)/sizeof(arr[0])-a-1;j++)
        {
            if(arr[j] > arr[j + 1])
            {
                int temp = arr[j+1];
                arr[j + 1] = arr[j];
                arr[j] = temp;
            }
        }
    }
    cout << "the latter array is as follows" << endl;
    for(int b = 0;b<10;b++)
    {
        cout << arr[b];
    }
    cout << endl;

    return 0;
}
