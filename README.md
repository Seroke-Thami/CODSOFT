
#include <iostream>
#include <cstdlib>  
#include <ctime>    
using namespace std;
int main() {

    srand(time(0));
    int secretNumber = rand() % 100 + 1;

    int guess;
    int count = 0;
    cout << "Welcome to the Number Guessing Game!\n";
    cout << "Try to guess the number between 1 and 100.\n\n";

    do {
        cout << "Enter your guess: ";
        cin >> guess;

        if (guess == secretNumber) {
            cout << "Congratulations! You guessed the correct number in " << count << " attempts.\n";
        }
        else if (guess < secretNumber) {
            cout << "Too low. Try again.\n";
        }
        else {
            cout << "Too high. Try again.\n";
        }

        count++;

    } while (guess != secretNumber);

    return 0;
}
