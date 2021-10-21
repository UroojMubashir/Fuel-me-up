#include <iostream>
using namespace std;
int main()
{
    cout << "Enter the number of litres you want to fill:\n";
    double lit, c;


    std::cin >> lit;
    //Using the cin.fail function (when user enters alphabet instead of numbers)
    if (std::cin.fail())
    {
        std::cin.clear();
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
        std::cout << "Incorrect command\n: ";
    }

    else {
        cout << "You have selected " << lit << " litres\n";
        cout << "Now select the type of fuel you want \n";
        cout << "Enter 'p' for Petrol\n Enter'd' for Diesel\n";
        char fuel;
        cin >> fuel;
        switch (fuel)
        {
        case 'P':
        case 'p':
        {

            cout << "You have selected Petrol \n ";

            c = lit * 0.7;
            cout << "\nThe price per litres is 0.7 now the total is " << c << " AED" << endl;
            break;
        }
        case 'd':
        case 'D':
        {
            cout << "You have selected Diesel  ";

            c = lit * 0.3;
            cout << "\nThe price per litres is 0.3 now the total is " << c << " AED" << endl;
            break;

            break;
        }

        default:
        {
            cout << "Incorrect command";
            break;
        }

        }
    }
}
