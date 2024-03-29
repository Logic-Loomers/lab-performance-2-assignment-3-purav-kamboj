On a specific day, the exchange rates were as follows: the British pound was valued at $1.487 U.S., the French franc at $0.172, the German deutschemark at $0.584, and the Japanese yen at $0.00955. Write a program that prompts the user to input an amount in U.S. dollars. The program should then display this amount converted into these four other currencies. Test the program by inputting various dollar amounts and ensuring that the conversions to British pounds, French francs, German deutschemarks, and Japanese yen are accurate. Additionally, test the program with negative dollar amounts to verify that it handles invalid input appropriately.


#include <iostream>
using namespace std;

double convertToPounds(double dollars)
{
    return dollars * 1.487;
}

double convertToFrancs(double dollars)
{
    return dollars * 0.172;
}

double convertToDeutschemarks(double dollars)
{
    return dollars * 0.584;
}

double convertToYen(double dollars)
{
    return dollars * 0.00955;
}

int main()
{
    cout << "Name- Purav Kamboj" << endl;
    cout << "Roll no.- 2310997227" << endl;
    cout << endl;

    double dollars;
    while (true)
    {
        cout << endl;
        cout << "Enter the amount in U.S. dollars (-ve value to quit): ";
        cin >> dollars;
        if (dollars < 0)
        {
            cout << endl
                 << "----Invalid input----" << endl;
            break;
        }
        double pounds = convertToPounds(dollars);
        double francs = convertToFrancs(dollars);
        double deutschemarks = convertToDeutschemarks(dollars);
        double yen = convertToYen(dollars);
        cout << "Amount in British Pounds: " << pounds << endl;
        cout << "Amount in French Francs: " << francs << endl;
        cout << "Amount in German Deutschemarks: " << deutschemarks << endl;
        cout << "Amount in Japanese Yen: " << yen << endl;
    }
    return 0;
}
