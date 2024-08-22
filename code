#include <iostream>
#include <string>

using namespace std;

bool isNumberString(const string& s) {
    for (char c : s) {
        if (!isdigit(c))
            return false;
    }
    return true;
}

bool isValidCreditCardNumber(const string& ccNumber) {
    int len = ccNumber.length();
    int doubleEvenSum = 0;

    for (int i = len - 2; i >= 0; i -= 2) {
        int digit = (ccNumber[i] - '0') * 2;
        if (digit > 9) {
            digit = digit / 10 + digit % 10;
        }
        doubleEvenSum += digit;
    }

    for (int i = len - 1; i >= 0; i -= 2) {
        doubleEvenSum += ccNumber[i] - '0';
    }

    return (doubleEvenSum % 10 == 0);
}

int main() {
    string ccNumber;

    cout << "This program uses the Luhn Algorithm to validate a credit card number." << endl;
    cout << "You can enter 'exit' anytime to quit." << endl;

    while (true) {
        cout << "Please enter a credit card number to validate: ";
        cin >> ccNumber;

        if (ccNumber == "exit")
            break;

        if (!isNumberString(ccNumber)) {
            cout << "Bad input! Please enter only numerical digits." << endl;
            continue;
        }

        bool isValid = isValidCreditCardNumber(ccNumber);
        cout << (isValid ? "Valid!" : "Invalid!") << endl;
    }

    return 0;
}
