#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int choice;
    double amount, converted;
    
    // Example rates: 1 USD to other currencies
    const double INR = 83.25;
    const double EUR = 0.92;
    const double GBP = 0.79;
    const double JPY = 155.32;

    cout << fixed << setprecision(2);
    cout << "----- Currency Converter -----" << endl;
    cout << "Convert from USD to:" << endl;
    cout << "1. INR (Indian Rupee)" << endl;
    cout << "2. EUR (Euro)" << endl;
    cout << "3. GBP (British Pound)" << endl;
    cout << "4. JPY (Japanese Yen)" << endl;
    cout << "Enter your choice (1-4): ";
    cin >> choice;

    cout << "Enter amount in USD: ";
    cin >> amount;

    switch (choice) {
        case 1:
            converted = amount * INR;
            cout << "INR: ₹" << converted << endl;
            break;
        case 2:
            converted = amount * EUR;
            cout << "EUR: €" << converted << endl;
            break;
        case 3:
            converted = amount * GBP;
            cout << "GBP: £" << converted << endl;
            break;
        case 4:
            converted = amount * JPY;
            cout << "JPY: ¥" << converted << endl;
            break;
        default:
            cout << "Invalid choice!" << endl;
    }

    return 0;
}
