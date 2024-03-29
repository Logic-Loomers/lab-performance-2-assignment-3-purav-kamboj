[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/Fmb6W2KK)
Design a C++ program for an employee payroll system. Create classes for Employee and Payroll. Users can add employees, enter hours worked, calculate salaries, and generate payroll reports.


#include <iostream>
using namespace std;

class Employee
{

public:
    char name[20];
    int phone;
    std::string designation;
    std::string address;
    double salary;
    int hoursWorked;

    void get()
    {
        cout << "Enter Employee Name: ";
        cin >> name;
        cout << "Enter Employee Designation: ";
        cin >> designation;
        cout << "Enter Employee City: ";
        cin >> address;
        cout << "Enter Employee Phone number: ";
        cin >> phone;
        cout << "Enter Salary per hour: ";
        cin >> salary;
        cout << "Enter number of hours worked: ";
        cin >> hoursWorked;
    }
};

class Payroll : public Employee
{
public:
    void display()
    {
        cout << "Employee Name: ";
        cout << name;
        cout << endl;

        cout << "Employee Designation: ";
        cout << designation;
        cout << endl;

        cout << "Employee City: ";
        cout << address;
        cout << endl;

        cout << "Employee Phone number: ";
        cout << phone;
        cout << endl;

        cout << "Employee Total Salary: ";
        cout << salary * hoursWorked;
        cout << endl;
    }
};

int main()
{
    cout << "Name- Purav Kamboj" << endl;
    cout << "Roll no.- 2310997227" << endl;
    cout << endl;

    Payroll obj1, obj2, obj3, obj4, obj5;
    Payroll obj[] = {obj1,
                     obj2,
                     obj3,
                     obj4,
                     obj5};

    cout << "----Enter  details of Employees---- " << endl;
    for (int i = 0; i < 3; i++)
    {
        obj[i].get();
        cout << endl;
    }


    cout << "----Payroll Slips of Employees---- " << endl;
    for (int i = 0; i < 3; i++)
    {
        obj[i].display();
        cout << endl;
    }

    return 0;
}
