//
//  main.cpp
//  addressbook system
//
//  Created by Haoyang Chen on 2020/11/9.
//

#include <iostream>
#include <string>
#include <stdlib.h>
using namespace std;
#define Max 1000// defining the maximun of the person in the addressbook
struct Person//the struct of the people in the addressbook
{
    string m_Name;
    int m_Sex;
    int m_Age;
    string m_Phone;
    string m_Address;
};
struct Addressbook//the struct of the addressbook
{
    struct Person personArray[Max];
    int m_size;//current size of the addressbook
};
void addPerson(Addressbook * abs)//the func to add persons
{
    if (abs->m_size==Max)//if the current number is the maximum,break
    {
        cout << "full!!" << endl;
        return;
    }
    string name;//entering the string name
    cout << "please enter a name" << endl;
    cin >> name;
    abs->personArray[abs->m_size].m_Name = name;
    cout << "please enter the sex" << endl;//entering the int sex of 1&2
    cout << "1---male" << endl;
    cout << "2---female" << endl;
    int sex=0;
    while (1)
    {
        cin >> sex;
        if (sex==1||sex==2)
        {
            abs->personArray[abs->m_size].m_Sex = sex;
            break;
        }
            cout << "error" <<endl;
    }
    cout << "please enter the age" << endl;//entering the int of the age
    int age = 0;
    cin >>age ;
    abs->personArray[abs->m_size].m_Age = age;
    cout << "please enter the tel" << endl;//entering the string of the phone number
    string phone;
    cin >> phone;
    abs->personArray[abs->m_size].m_Phone = phone;
    cout << "please enter the address" << endl;//entering the string of the address
    string address;
    cin >> address;
    abs->personArray[abs->m_size].m_Address = address;
    abs->m_size++;//when a new person is added, the current size ++
    cout << "successfully added" << endl;
}
void showperson(Addressbook * abs)//a func to show all the persons in the addressbook
{
    if (abs->m_size == 0)
    {
        cout << "no contact person detected" << endl;
    }
    else{
        for (int i=0;i<abs->m_size;i++)//cout every person and info one by one
        {
            cout << "Name:" << abs->personArray[i].m_Name <<"\t";
            cout << "Age:" << abs->personArray[i].m_Age <<"\t";
            cout << "Sex:" << (abs->personArray[i].m_Sex == 1 ?"male":"female" )<<"\t";
            cout << "Tel:" << abs->personArray[i].m_Phone <<"\t";
            cout << "Address:" << abs->personArray[i].m_Address <<endl;
        }
    }
}
int exist(Addressbook * abs ,string name)//a func to judge whether the entered person exist
{
    for (int i = 0;i < abs->m_size;i++)//search for the person one by one
    {
        if (abs->personArray[i].m_Name == name)
        {
            return i;//return the person's number in the array
        }
    }
    return -1;
}
void deletePerson(Addressbook * abs)//a func to remove a person
{
    cout << "please enter the name of the person to delete" <<endl;
    string name;
    cin >> name;
    int ret = exist(abs, name);//using an int ret to record the returned number as the location
    if (ret==-1)
    {
        cout << "NULL" <<endl;
    }
    else{
        for (int i = ret;i<abs->m_size;i++)
        {
            abs->personArray[i] = abs->personArray[i+1];//use the later info to replace the former
        }
        abs->m_size--;//current size minus one
        cout << "successfully deleted" <<endl;
    }
}
void findPerson(Addressbook * abs)//a func to find a certain person
{
    cout << "please enter the person to find" <<endl;
    string name;
    cin >> name;
    int ret = exist(abs, name);//record location
    if (ret != -1)//give out the searched person's info
    {
        cout << "Name:" << abs->personArray[ret].m_Name <<"\t";
        cout << "Age:" << abs->personArray[ret].m_Age <<"\t";
        cout << "Sex:" << (abs->personArray[ret].m_Sex == 1 ?"male":"female" )<<"\t";
        cout << "Tel:" << abs->personArray[ret].m_Phone <<"\t";
        cout << "Address:" << abs->personArray[ret].m_Address <<endl;
    }
    else{
        cout << "NULL" <<endl;
    }
}
void modifyPerson(Addressbook * abs)//to modify a person's info
{
    cout << "please enter the person to modify" <<endl;
    string name;
    cin >> name;
    int ret = exist(abs, name);//record location
    if (ret != -1)
    {
        string name;
        cout << "please enter a name" << endl;
        cin >> name;
        abs->personArray[ret].m_Name = name;
        cout << "please enter the sex" << endl;
        cout << "1---male" << endl;
        cout << "2---female" << endl;
        int sex = 0;
        while (1)//judge whether entered the right sex
        {
            cin >>sex;
            if(sex==0||sex==2)
            {
                abs->personArray[ret].m_Sex = sex;
                break;
            }
            cout << "error" <<endl;
        }
        cout << "please enter the age" <<endl;
        int age = 0;
        cin >> age;
        abs->personArray[ret].m_Age = age;
        cout << "please enter the tel" <<endl;
        string tel;
        cin >> tel;
        abs->personArray[ret].m_Phone = tel;
        cout << "please enter the address" <<endl;
        string address;
        cin >> address;
        abs->personArray[ret].m_Address = address;
    }
    else{
        cout << "NULL" <<endl;
    }
}
void clear(Addressbook * abs)//a func to remove all the data
{
    abs->m_size = 0;//reduce the size to zero
    cout << "successfully cleared" <<endl;
}
void showmenu()
{
    cout << "1.add" << endl;//showing the menu
    cout << "2.show" << endl;
    cout << "3.delete" << endl;
    cout << "4.search" << endl;
    cout << "5.change" << endl;
    cout << "6.clear" << endl;
    cout << "0.exit" <<endl;
}
int main(int argc, const char * argv[])
{
    Addressbook abs;//creating an abs under the struct of Addressbook
    abs.m_size=0;//make sure you have initiallized this one!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
    while (1)//making sure that the programme keeps running
    {
    showmenu();//running the func of menu
        int choice=0;
        cin >> choice;//deciding which function to use
        switch (choice)
        {
            case 1://to add a new person to the addressbook
                addPerson(&abs);
                break;
            case 2://to review the whole of the addressbook
                showperson(&abs);
                break;
            case 3://to remove a person from the addressbook
             deletePerson(&abs);
                break;
            case 4://to locate a person in the addressbook
                findPerson(&abs);
                break;
            case 5://to change a person's info
                modifyPerson(&abs);
                break;
            case 6://to remove all the persons from the addressbook
                clear(&abs);
                break;
            case 0://to exit the system
                cout << "bye" << endl;
                return 0;
                break;
            default:
                break;
        }
    }
    return 0;
}
