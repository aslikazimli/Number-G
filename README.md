#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;
int main() {
    srand(time(0));
    int secretNumber = rand() % 100 +1;
    int guess;
    int attempts = 0;
    cout << "I have chosen a number between 1 and 100.\n";
    cout << "Try to guess it!.\n";
    do {
        cout <<"Enter your guess: ";
        cin >> guess;
        attempts++;
        if (guess > secretNumber) {
            cout << "To high!\n";
        } else if (guess < secretNumber) {
            cout << "Too low!\n";
        } else {
            cout << "Correct! You guessed it in " << attempts << " attempts.\n";
        }
    } while (guess != secretNumber);
    return 0;
}
