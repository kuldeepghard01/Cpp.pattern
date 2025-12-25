#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));
    int secret = rand() % 100 + 1;
    int guess;

    cout << "Guess the number (1 to 100): ";

    while (true) {
        cin >> guess;

        if (guess > secret) {
            cout << "Too High! Try again: ";
        }
        else if (guess < secret) {
            cout << "Too Low! Try again: ";
        }
        else {
            cout << "🎉 You Win! Correct number.";
            break;
        }
    }

    return 0;
}
