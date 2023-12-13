//# CODSOFT
#include <iostream>
#include <stdexcept>
using namespace std;

int main() {
    string menu[] = { "fruits", "chicken", "fish", "cake" };

    try {
        int x;
        cout << "Enter a number to select a menu item: ";
        cin >> x;

        if (x < 0 || x >= sizeof(menu) / sizeof(menu[0])) {
            throw out_of_range("404 - not found");
        }

        cout << "You selected: " << menu[x] << endl;
    }
    catch (const out_of_range& e) {
        cerr << e.what() << endl;
    }
    catch (...) {
        cerr << "An unknown error occurred." << endl;
    }

    return 0;
}
